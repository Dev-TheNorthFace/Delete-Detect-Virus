# 🚨 Comment supprimer un Auto-Réplicant (ver informatique) ? 🦠💻

Si votre ordinateur est infecté par un Auto-Réplicant, il est crucial d’agir rapidement pour éviter qu’il ne se propage à d’autres appareils. Voici les étapes détaillées pour s’en débarrasser.

## 🛠 Étape 1 : Déconnecter l'ordinateur du réseau 🌐❌
➡ **Objectif :** Empêcher la propagation du ver.
- Débranchez le câble Ethernet 🔌.
- Désactivez le Wi-Fi 📶❌ sur l'ordinateur infecté.
- Si possible, mettez l’appareil en mode avion ✈️.

## 🔎 Étape 2 : Analyser et supprimer le ver avec un antivirus 🛡️
➡ **Objectif :** Détecter et éradiquer le programme malveillant.
- Utilisez un antivirus à jour (Windows Defender, Bitdefender, Malwarebytes, Kaspersky...).
- Faites une analyse complète 🔍 (et non rapide).
- Supprimez les fichiers détectés 🗑️ et redémarrez l’ordinateur.

💡 **Si le ver empêche l’installation ou l’exécution de l’antivirus :**
🔹 **Redémarrez en mode sans échec avec prise en charge réseau 📌 :**

**Windows :**
- Redémarrez et appuyez sur `F8` ou `Shift + F8` avant le logo Windows.
- Sélectionnez "Mode sans échec avec prise en charge réseau".

**Mac :**
- Redémarrez et maintenez `Shift` enfoncé.
- Ouvrez un antivirus et lancez une analyse.

## 🔥 Étape 3 : Vérifier et supprimer manuellement les fichiers suspects 🗂️
➡ **Objectif :** Éliminer tout reste du ver.

📌 **Sur Windows :**
- Ouvrez le Gestionnaire des tâches (`Ctrl + Shift + Échap`) et cherchez des processus inconnus 🕵️.
- Utilisez **Autoruns (Microsoft)** pour voir les programmes qui se lancent au démarrage.
- Vérifiez les dossiers système 📂 :
  - `C:\Windows\System32\`
  - `C:\Users\VotreNom\AppData\Local\Temp\`
  - `C:\ProgramData\`

Commandes utiles 🖥️ :
- `tasklist` (liste des processus actifs)
- `netstat -ano` (voir les connexions réseau suspectes)
- `wmic process get description,executablepath` (trouver l’emplacement des processus)

📌 **Sur Mac :**
- Ouvrez **Moniteur d’Activité** (`Cmd + Espace`, tapez "Moniteur d’Activité").
- Cherchez un processus suspect et forcez l’arrêt 🛑.
- Supprimez les fichiers suspects dans :
  - `/Library/LaunchAgents/`
  - `/Library/LaunchDaemons/`
  - `/Users/VotreNom/Library/Application Support/`

## 🔐 Étape 4 : Vérifier et nettoyer le registre (Windows uniquement)
➡ **Objectif :** Supprimer les entrées du ver dans le registre système.
⚠ **Attention ! Toute erreur peut endommager le système.** ⚠

- Tapez `regedit` dans Exécuter (`Windows + R`).
- Allez à `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run`.
- Recherchez des entrées suspectes et supprimez-les.
- Redémarrez votre PC.

## 🏆 Étape 5 : Mettre à jour et sécuriser son système 🔒
➡ **Objectif :** Éviter une réinfection.
✔ Mettez à jour Windows/Mac et tous vos logiciels 🛠️.
✔ Activez un pare-feu 🔥.
✔ Changez vos mots de passe 🔑.
✔ Scannez votre réseau avec Wireshark ou Netstat.

🆘 **Si le ver persiste ❌**
➡ **Dernier recours : Réinstaller le système**