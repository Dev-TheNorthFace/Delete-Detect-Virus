## 1️⃣ Déconnecte-toi d'Internet immédiatement

📌 Pourquoi ?

Si le keylogger envoie tes frappes à un serveur distant, déconnecter Internet empêche la fuite de données.
✅ Désactive le Wi-Fi et débranche le câble Ethernet.
✅ Ne te reconnecte pas avant d’avoir supprimé l’infection.

---

## 2️⃣ Redémarre en mode sans échec

📌 Pourquoi ?

Le mode sans échec empêche la plupart des keyloggers de s’exécuter.

➡️ Comment faire ?

### Windows 10/11
1. `Win + R` → tape `msconfig` → Onglet **Démarrer** → Coche **Démarrage sécurisé + Réseau** → Redémarrer.

### Windows 7/8
1. Appuie sur `F8` avant le démarrage → Sélectionne **Mode sans échec avec prise en charge réseau**.

---

## 3️⃣ Identifier et supprimer le keylogger manuellement

### 🔍 Vérifier les processus en cours
1. Ouvre le **Gestionnaire des tâches** (`Ctrl + Shift + Échap`).
2. Cherche des noms suspects comme :
   - `WindowsUpdate.exe`, `svchost.exe` (hors de System32).
   - `KeyLogger.exe`, `monitor.exe`, `Stealth.exe`, `Logger.exe`, `SystemSecure.exe`.
3. Fais un **clic droit** → **Ouvrir l’emplacement du fichier** → Si le fichier est dans `AppData` ou `System32`, c'est louche.
4. **Arrête le processus** (Clic droit → Fin de tâche).

### 🔍 Vérifier les fichiers cachés
1. Ouvre l’**Explorateur de fichiers** → **Affichage** → Coche **"Fichiers cachés"**.
2. Va dans :
   - `C:\Users\[TON_USER]\AppData\Roaming\`
   - `C:\Users\[TON_USER]\AppData\Local\`
   - `C:\Windows\System32\`
3. Cherche des fichiers récents et suspects (`.exe`, `.dll`, `.log`).
4. Supprime-les définitivement (`Shift + Suppr`).

### 🔍 Vérifier les tâches planifiées
📌 Certains keyloggers utilisent des **tâches planifiées** pour redémarrer après suppression.

➡️ **Ouvre l’Observateur d’événements** :
- `Win + R` → tape `taskschd.msc` → **Planificateur de tâches**.
- Cherche une tâche inconnue qui exécute un `.exe` suspect.
- **Supprime la tâche** (Clic droit → Supprimer).

### 🔍 Vérifier les logiciels installés
📌 Certains keyloggers s’installent comme des logiciels normaux.

➡️ Va dans :
- `Win + R` → tape `appwiz.cpl` (ouvre **"Programmes et fonctionnalités"**).
- Cherche un programme suspect ou récemment installé.
- Si tu vois un logiciel inconnu, **désinstalle-le immédiatement**.

---

## 4️⃣ Supprimer le keylogger avec un antivirus & anti-malware

📌 Pourquoi ?

Même après suppression manuelle, un keylogger peut avoir des restes.
Un antivirus détectera les fichiers cachés et les supprimera définitivement.

✅ **Lance un scan complet avec** :
1. **Windows Defender** :
   - Paramètres → Mise à jour et sécurité → Sécurité Windows → **Analyse complète**.
2. **Malwarebytes** (gratuit) :
   - Télécharge depuis le site officiel et fais une **analyse approfondie**.
3. **HitmanPro** *(optionnel, mais puissant)* :
   - Scan cloud avancé pour détecter les logiciels espions.

💡 **Si ton antivirus détecte des fichiers**, mets-les en **quarantaine** ou **supprime-les**.

---

## 5️⃣ Vérifier et nettoyer le Registre Windows

📌 Certains keyloggers laissent des traces dans le **Registre** pour se relancer.

➡️ **Ouvre l’Éditeur du Registre** :
- `Win + R` → tape `regedit` → Entrée.

1. Va dans ces emplacements :
   - `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run`
   - `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`
2. Cherche des **entrées inconnues** pointant vers un `.exe` suspect.
3. **Supprime-les** (Clic droit → Supprimer).

💡 **Outil recommandé** : [CCleaner](https://www.ccleaner.com/) → Pour nettoyer le registre plus facilement.

---

## 6️⃣ Vérifier les connexions réseau

📌 Si un keylogger envoie des données, il doit établir une connexion externe.

➡️ **Ouvre une console PowerShell en mode administrateur** et tape :
```powershell
netstat -ano | findstr :80
```
Regarde s’il y a une **IP suspecte** connectée à ton PC.
Copie l’adresse IP et recherche-la sur [Whois Lookup](https://who.is/) pour voir si elle est légitime.

💡 **Outil recommandé** : [Wireshark](https://www.wireshark.org/) pour analyser le trafic en détail.

---

## 7️⃣ Changer tous tes mots de passe

📌 Si un keylogger a volé tes frappes clavier, tes comptes sont potentiellement compromis.

✅ **Depuis un autre appareil sécurisé, change tes mots de passe** :
- **Messagerie** (*Gmail, Outlook, etc.*).
- **Réseaux sociaux** (*Facebook, Instagram, Twitter, Discord*).
- **Banque & paiements** (*PayPal, Amazon, cartes bancaires*).

💡 **Active l’authentification à deux facteurs (2FA)** sur tous tes comptes.

---

## 8️⃣ Surveiller son PC après suppression

📌 Même après avoir supprimé un keylogger, surveille ton PC pour être sûr qu’il n’y a plus de trace.

✅ **Outils recommandés pour le monitoring** :
- **GlassWire** : Montre les applications qui envoient des données sur Internet.
- **Process Explorer** : Pour surveiller les processus en arrière-plan.
- **SpyShelter** : Détecte les tentatives d’enregistrement clavier.

---

## 9️⃣ Réinstaller Windows (en dernier recours)

📌 **Si le keylogger est bien caché, le seul moyen sûr à 100% est de réinstaller Windows.**

➡️ **Comment faire ?**
1. **Sauvegarde tes fichiers importants** sur un disque externe.
2. **Télécharge l’outil de réinstallation de Windows** depuis le site Microsoft.
3. **Effectue une installation propre** en formatant le disque dur.

---

## 🔥 Résumé des étapes :
✅ Déconnecte-toi d’Internet.
✅ Redémarre en mode sans échec.
✅ Supprime manuellement les fichiers suspects.
✅ Désinstalle les logiciels suspects.
✅ Scan complet avec un antivirus & anti-malware.
✅ Nettoie le Registre Windows.
✅ Vérifie les connexions réseau.
✅ Change tous tes mots de passe.
✅ Surveille ton PC après suppression.
✅ Réinstalle Windows si nécessaire.