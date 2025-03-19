# 🛑 Comment supprimer un ransomware ? 🦠🔒

Si vous êtes infecté par un ransomware, suivez ces étapes immédiatement pour limiter les dégâts et essayer de récupérer vos fichiers. 🚨

**⚠️ Ne payez pas la rançon !** Il n’y a aucune garantie que les cybercriminels vous rendront vos fichiers.

## 🏆 Étape 1 : Déconnecter l’ordinateur 🌐❌

- Désactivez le Wi-Fi et débranchez le câble Ethernet pour empêcher le ransomware de se propager et de communiquer avec ses serveurs.
- Si le ransomware est actif, éteignez immédiatement votre ordinateur en maintenant le bouton d’alimentation.

## 🔧 Étape 2 : Démarrer en mode sans échec 🖥️

Le mode sans échec empêche le ransomware de fonctionner au démarrage.

### Sous Windows :
1. Redémarrez votre PC et appuyez plusieurs fois sur **F8** ou **Shift + F8** avant l’apparition du logo Windows.
2. Sélectionnez **"Mode sans échec avec prise en charge réseau"**.

### Sous Mac :
1. Éteignez votre Mac et rallumez-le en maintenant la touche **Shift**.

## 💪 Étape 3 : Scanner et supprimer le ransomware 🔎

Utilisez un ou plusieurs outils spécialisés pour détecter et supprimer le ransomware :

### 🔹 Antivirus classiques :
- Windows Defender (Windows 10/11)
- Bitdefender
- Kaspersky
- [Malwarebytes](https://fr.malwarebytes.com/)

### 🔹 Outils anti-ransomware spécialisés :
- [Emsisoft Decryptor](https://www.emsisoft.com/ransomware-decryption-tools/)
- Avast Ransomware Removal
- Trend Micro Ransomware File Decryptor

➔ **Faites un scan complet et supprimez les menaces détectées.**

## 🖽 Étape 4 : Supprimer manuellement les fichiers du ransomware

### 1⃣ Supprimez les fichiers malveillants du démarrage :

- Ouvrez l’Éditeur du Registre (**Win + R**, tapez `regedit`).
- Allez dans :
  ```
  HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
  ```
- Supprimez les entrées suspectes.

### 2⃣ Vérifiez les tâches planifiées :

- Tapez `taskschd.msc` dans la barre de recherche Windows et vérifiez si des tâches inconnues lancent des programmes suspects.

### 3⃣ Supprimez les fichiers suspects :

- Allez dans :
  ```
  C:\Users\VotreNom\AppData\Roaming
  C:\Users\VotreNom\AppData\Local
  C:\ProgramData
  ```
- Supprimez les fichiers récemment créés qui vous semblent étranges.

## 🔑 Étape 5 : Tenter de récupérer vos fichiers chiffrés

### 🤌 Méthode 1 : Utiliser un déchiffreur gratuit
- Allez sur [No More Ransom](https://www.nomoreransom.org/) pour voir si un outil de déchiffrement est disponible pour votre ransomware.
- Essayez [ID Ransomware](https://id-ransomware.malwarehunterteam.com/) pour identifier le type de ransomware et obtenir des solutions.

### 💾 Méthode 2 : Restaurer à partir d’une sauvegarde
- Si vous avez une sauvegarde locale ou sur le cloud, restaurez vos fichiers **après avoir totalement supprimé le ransomware**.

### 🔄 Méthode 3 : Récupérer des fichiers supprimés
- Certains ransomwares effacent les fichiers originaux après chiffrement.
- Essayez un outil de récupération de données comme **Recuva** ou **EaseUS Data Recovery**.

## 🚀 Étape 6 : Protéger son PC contre une réinfection

✔ Mettez à jour Windows et tous vos logiciels 🔄.
✔ Utilisez un bon antivirus et activez Windows Defender 🛡️.
✔ Activez la protection contre le chiffrement de fichiers (**Windows Defender > Sécurité de l’appareil**).
✔ Faites des sauvegardes régulières sur un disque dur externe 💀.
✔ Ne cliquez jamais sur des pièces jointes suspectes 📎❌.

---

En suivant ces étapes, vous maximisez vos chances de **supprimer le ransomware** et de **récupérer vos fichiers** sans payer la rançon. 🚫💰