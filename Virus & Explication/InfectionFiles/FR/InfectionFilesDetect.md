# 📌 Détection d'un infecteur de fichiers qui transforme des .exe en .dll pour s'auto-propager

Un infecteur de fichiers est un type de malware qui modifie des exécutables légitimes pour insérer son propre code malveillant. Dans le cas que tu évoques, il change des fichiers `.exe` en `.dll`, ce qui peut lui permettre de s'exécuter discrètement et de se propager sur le système.

---

## 🔎 Comment détecter un tel malware ?

### 1️⃣ Surveiller les modifications suspectes de fichiers

💡 **Objectif** : Identifier les fichiers `.exe` transformés en `.dll`

📌 **Méthodes** :

✅ Utiliser PowerShell pour détecter les fichiers modifiés récemment :

```powershell
Get-ChildItem -Path C:\ -Recurse -Filter *.dll | Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-1) }
```

✅ Comparer les extensions des fichiers avant et après une infection possible.
✅ Vérifier les répertoires sensibles (`C:\Windows\System32`, `C:\Program Files`, etc.) pour repérer des modifications anormales.

### 2️⃣ Comparer les empreintes numériques (hash) des fichiers

💡 **Objectif** : Vérifier si un fichier a été modifié par un virus

📌 **Méthodes** :

✅ Avant une infection, enregistrer les hashes des fichiers `.exe` avec cette commande :

```powershell
Get-FileHash C:\Path\to\file.exe -Algorithm SHA256
```

✅ Après suspicion d’infection, recalculez les hashes et comparez-les.
🔴 **Si le hash change alors que le fichier n’a pas été mis à jour, cela peut signaler une infection !**

### 3️⃣ Surveiller les accès aux fichiers et à la mémoire

💡 **Objectif** : Repérer les programmes qui modifient des fichiers `.exe`

📌 **Outils recommandés** :

✅ **Sysinternals Process Monitor (ProcMon)** → Montre quelles applications modifient les fichiers `.exe` ou `.dll`
✅ **Windows Event Viewer** → Activez l’audit des accès aux fichiers pour enregistrer les modifications.

📌 **Actions** :

- Ouvrir **ProcMon**, appliquer un filtre sur `Path` contenant `.exe` et `.dll`.
- Observer si un programme inconnu ouvre puis modifie des `.exe` avant de les renommer en `.dll`.

### 4️⃣ Détection comportementale

💡 **Objectif** : Identifier un comportement suspect des processus en cours

📌 **Méthodes** :

✅ **Process Explorer** → Vérifier quelles DLL sont chargées par chaque processus.
✅ **Autoruns** → Repérer des DLL inconnues qui se chargent au démarrage.
✅ **Windows Defender ATP (ou autre EDR)** → Détecter les accès suspects aux fichiers système.

🔍 **Indicateurs d’infection** :

🔴 Un programme qui modifie des exécutables alors qu’il ne devrait pas.
🔴 Un fichier `.dll` qui a récemment remplacé un `.exe` dans un dossier système.
🔴 Un programme non signé ou inconnu qui s’exécute en arrière-plan.

### 5️⃣ Analyse avec un antivirus et une sandbox

💡 **Objectif** : Confirmer qu’un fichier suspect est infecté

📌 **Méthodes** :

✅ Scanner le fichier suspect avec **VirusTotal**
✅ Utiliser une **machine virtuelle (VM)** pour tester l’exécution du fichier sans risquer d’infecter le système principal
✅ Analyser la mémoire vive avec **GMER** ou **Volatility** pour détecter des processus cachés

---

## 🚨 Que faire si une infection est détectée ?

### 🛑 Étapes d’urgence

1️⃣ **Déconnecter l’ordinateur d’Internet** pour éviter la propagation.
2️⃣ **Mettre en quarantaine les fichiers suspects** avec un antivirus.
3️⃣ **Démarrer en mode sans échec** et scanner le PC avec un outil comme **Malwarebytes**.
4️⃣ **Restaurer les fichiers système infectés** avec :

```cmd
sfc /scannow
```

5️⃣ **Réinstaller les exécutables modifiés** à partir d’une source fiable.

---

## 🛡️ Prévention pour éviter les futures infections

✅ **Désactiver l’exécution automatique des DLL inconnues**
✅ **Utiliser un compte utilisateur avec des permissions limitées**
✅ **Activer l’UAC (User Account Control)** pour éviter l’exécution automatique des malwares
✅ **Garder un antivirus à jour et activer les protections heuristiques**