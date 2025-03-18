# 🚨 Comment supprimer un infecteur de fichiers qui modifie les .exe en .dll ? 🚨

Si ton système est infecté par un malware qui modifie les fichiers `.exe` en `.dll` pour se propager, il faut agir rapidement pour éviter la contamination d'autres fichiers et empêcher le malware de se réinstaller.

---

## 🛑 1. Isolation immédiate de la machine

Avant toute action, isole l’ordinateur pour éviter que le virus ne se propage via le réseau ou des périphériques externes :

- 🔌 Déconnecte Internet (Wi-Fi et câble Ethernet)
- 🔒 Désactive les partages réseau
- 🖥️ Évite de brancher des clés USB ou des disques durs externes

---

## 🔍 2. Identifier les fichiers infectés

Avant de supprimer le malware, il faut localiser les fichiers infectés. Voici plusieurs méthodes :

### 📌 Avec l’Explorateur de fichiers et PowerShell

Lister les fichiers `.dll` récemment modifiés :

```powershell
Get-ChildItem -Path C:\ -Recurse -Filter *.dll | Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-3) }
```

Lister les fichiers `.exe` récemment modifiés :

```powershell
Get-ChildItem -Path C:\ -Recurse -Filter *.exe | Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-3) }
```

### 📌 Avec un antivirus / antimalware

- ✅ **Windows Defender** → Faire un scan complet
- ✅ **Malwarebytes** → Détecte les trojans et fichiers modifiés
- ✅ **HitmanPro** → Bon pour éliminer les infections persistantes

---

## 🛠️ 3. Suppression du malware

### 🔹 Méthode 1 : Mode sans échec + suppression manuelle

1. Redémarre en **mode sans échec avec réseau** :  
   **Windows 10/11** : `Shift + Redémarrer` → *Dépannage* → *Options avancées* → *Paramètres de démarrage* → *Redémarrer* → Choisir **Mode sans échec avec réseau** (`F5`)
2. Ouvre le **Gestionnaire des tâches** (`Ctrl + Shift + Échap`)
3. Vérifie les **processus suspects** (ex: `randomname.dll` chargé dans `explorer.exe`). Utilise **Process Explorer (Sysinternals)** pour voir quelles DLL sont injectées.
4. **Arrête les processus suspects** :  
   → Clic droit → *Terminer la tâche*  
   → Supprime les fichiers infectés trouvés avec **PowerShell**

### 🔹 Méthode 2 : Suppression avec un antivirus bootable

Si le virus résiste à la suppression, utilise un **antivirus bootable** qui scanne ton disque avant le démarrage de Windows :

- ✅ **Kaspersky Rescue Disk**
- ✅ **ESET SysRescue Live**
- ✅ **Bitdefender Rescue CD**

**Étapes :**
1. Télécharge l’ISO sur un **autre PC propre**.
2. Mets-le sur une clé USB avec **Rufus**.
3. Démarre l’ordinateur infecté **depuis la clé** (via le BIOS).
4. Fais un **scan et supprime** les fichiers infectés.

### 🔹 Méthode 3 : Restaurer les fichiers système infectés

Si des fichiers Windows sont corrompus, il faut les restaurer.

#### 🔄 Avec `SFC` (System File Checker)

1. Ouvre `cmd` en tant qu’administrateur
2. Tape cette commande :

```cmd
sfc /scannow
```

3. Windows va vérifier et remplacer les fichiers système endommagés.

#### 🔄 Avec `DISM` (si `SFC` ne suffit pas)

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

---

## 🔥 4. Réinstaller les applications modifiées

Une fois le malware supprimé, les `.exe` modifiés doivent être remplacés par des versions propres :

- ✅ **Réinstalle les logiciels légitimes** depuis les sites officiels.
- ✅ **Si des fichiers Windows sont corrompus**, utilise `sfc /scannow` ou fais une **réinitialisation du PC**.

---

## 🔒 5. Prévenir une nouvelle infection

- 🔹 Active un **antivirus en temps réel**
- 🔹 Mets à jour **Windows et tes logiciels**
- 🔹 Active **Windows Defender Exploit Guard**
- 🔹 Désactive les **macros et l'exécution de DLL non signées**
- 🔹 **Crée des sauvegardes régulières** (images système et fichiers importants)