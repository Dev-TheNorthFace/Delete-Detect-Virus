## 🚨 Comment supprimer un Cheval de Troie (Trojan) ? 🛡🐴
Si vous avez détecté un Cheval de Troie sur votre PC, supprimez-le immédiatement pour éviter qu’il ne vole vos données ou donne un accès distant aux pirates. Suivez ces étapes dans l’ordre !

### 🚱 1. Déconnecter l’ordinateur d’Internet 🌐❌
- Désactivez le Wi-Fi et débranchez le câble Ethernet pour empêcher toute communication avec les pirates.
- Ne reconnectez pas Internet tant que le Trojan n’est pas supprimé !

### 🔥 2. Démarrer en mode sans échec 🖥️🚀
Le mode sans échec empêche le Cheval de Troie de fonctionner au démarrage.

**Sous Windows :**
- Redémarrez votre PC et appuyez plusieurs fois sur **F8** ou **Shift + F8** avant l’apparition du logo Windows.
- Sélectionnez **"Mode sans échec avec prise en charge réseau"**.

**Sous Mac :**
- Éteignez votre Mac et rallumez-le en maintenant la touche **Shift**.

### 🛡 3. Scanner et supprimer le Cheval de Troie avec un antivirus 🔎

#### 🔹 Utiliser Windows Defender (Gratuit) :
1. Tapez **"Sécurité Windows"** dans la barre de recherche Windows.
2. Allez dans **Protection contre les virus et menaces**.
3. Cliquez sur **"Analyse complète"** et laissez Windows scanner votre PC.
4. Supprimez toutes les menaces détectées.

#### 🔹 Utiliser un anti-malware spécialisé :
Si Windows Defender ne détecte rien, essayez un logiciel plus puissant :
- **Malwarebytes** [(Téléchargez ici)](https://www.malwarebytes.com/)
- **HitmanPro**
- **RogueKiller**
- **Kaspersky Removal Tool**

➡ Faites un scan complet et supprimez toutes les menaces détectées.

### 🖽 4. Supprimer le Trojan manuellement (si l’antivirus ne fonctionne pas)

#### 1️⃣ Supprimer les programmes malveillants du démarrage 🚀
- Tapez **msconfig** dans la barre de recherche Windows.
- Allez dans l’onglet **"Démarrage"** et désactivez tous les programmes suspects.
- Redémarrez votre PC.

#### 2️⃣ Vérifier et supprimer les fichiers du Trojan 🗂
Recherchez les fichiers malveillants dans ces dossiers :
```plaintext
C:\Users\VotreNom\AppData\Roaming
C:\Users\VotreNom\AppData\Local
C:\ProgramData
```
🔍 **Supprimez les fichiers inconnus créés récemment** (regardez la date de création).

#### 3️⃣ Supprimer les tâches planifiées suspectes 🕒
- Tapez **taskschd.msc** dans la barre de recherche Windows.
- Regardez les **tâches planifiées** et supprimez celles qui lancent des programmes inconnus.

#### 4️⃣ Supprimer les clés de registre malveillantes 🗝️
- Tapez **regedit** dans la barre de recherche Windows.
- Allez dans :
```plaintext
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
```
- **Supprimez les entrées suspectes** qui exécutent un fichier inconnu.

⚠️ **Attention !** Ne supprimez pas d’entrée système si vous n’êtes pas sûr.

#### 5️⃣ Supprimer les connexions réseau malveillantes 🌍
- Tapez **cmd.exe** et ouvrez l’Invite de commande.
- Entrez la commande :
```plaintext
netstat -ano
```
- **Recherchez des connexions suspectes actives en permanence.**
- Notez le **PID** (Process ID) du processus suspect.
- Tuez le processus en tapant :
```plaintext
taskkill /PID [NUMERO] /F
```

### 🔄 5. Redémarrer et vérifier que tout est propre
Après suppression du Trojan :
✔ Redémarrez votre PC.
✔ Faites un **nouveau scan antivirus** pour vérifier qu’il ne reste aucune menace.
✔ Reconnectez Internet uniquement si le scan est **100% propre**.

### 🚀 6. Se protéger contre une future infection
✔ **Mettez à jour Windows et votre antivirus** 🔄.
✔ **Activez Windows Defender ou installez un antivirus fiable** 🛡.
✔ **Ne téléchargez jamais de logiciels depuis des sites douteux** 🚫.
✔ **Ne cliquez jamais sur des pièces jointes suspectes dans vos emails** 📎❌.
✔ **Activez le pare-feu Windows pour bloquer les connexions suspectes** 🔥.
✔ **Faites des sauvegardes régulières de vos fichiers importants** 💾.