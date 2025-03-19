# 🚨 Comment supprimer un EmailWorm ? 🦠📧

Si vous êtes infecté par un EmailWorm, il est crucial d’agir rapidement pour stopper la propagation et sécuriser votre messagerie. Voici les étapes détaillées pour vous débarrasser de ce ver informatique.

## 🔍 Étape 1 : Déconnecter l’ordinateur du réseau 🌐❌
➡ **Objectif** : Empêcher le ver d’envoyer plus d’e-mails et de communiquer avec d’autres machines.

- Désactivez le Wi-Fi 📶❌ et débranchez le câble Ethernet 🔌.
- Évitez de reconnecter l’ordinateur à Internet tant que le ver n’est pas totalement supprimé.

## 🛡 Étape 2 : Scanner et supprimer l’EmailWorm avec un antivirus 🛠️
➡ **Objectif** : Identifier et éradiquer le ver automatiquement.

### ✅ 1. Lancez une analyse complète avec un antivirus à jour 🔎🛡️
- Utilisez Windows Defender, Malwarebytes, Bitdefender, Kaspersky, Avast ou tout autre antivirus fiable.
- Effectuez une analyse complète du système et non rapide.
- Supprimez ou mettez en quarantaine les fichiers infectés.

### ✅ 2. Si l’antivirus ne fonctionne pas, démarrez en mode sans échec 🔧
💡 *Le mode sans échec empêche le ver de s’exécuter au démarrage.*

**Sous Windows** :
- Redémarrez votre PC et appuyez sur **F8 / Shift + F8 / F4** avant l’apparition du logo Windows.
- Sélectionnez **"Mode sans échec avec prise en charge réseau"**.
- Lancez l’antivirus et supprimez les menaces détectées.

**Sous Mac** :
- Éteignez votre Mac et rallumez-le en maintenant la touche **Shift**.
- Une fois démarré, utilisez **Malwarebytes** ou un autre outil pour analyser et supprimer le ver.

## ✉️ Étape 3 : Sécuriser votre messagerie 🔐
➡ **Objectif** : Bloquer l’accès aux pirates et éviter toute réinfection.

### ✅ 1. Changez immédiatement votre mot de passe e-mail 🔑
- Utilisez un mot de passe long, unique et complexe.
- Activez **l’authentification à deux facteurs (2FA)** pour plus de sécurité.

### ✅ 2. Vérifiez si des règles suspectes ont été ajoutées à votre boîte e-mail 📬⚠️
Certains vers ajoutent des redirections automatiques vers d'autres adresses.

**Pour vérifier** :
- **Gmail** → *Paramètres > Filtres et adresses bloquées*
- **Outlook** → *Paramètres > Courrier > Règles*
- **Yahoo** → *Paramètres > Sécurité*

### ✅ 3. Vérifiez les connexions suspectes à votre compte 🌍
Consultez l’historique des connexions récentes et déconnectez les sessions inconnues.

**Exemples** :
- **Gmail** → *Détails des activités* en bas de la page principale.
- **Outlook** → *Sécurité > Activité de connexion récente*.

### ✅ 4. Prévenez vos contacts 📢
Envoyez un message à vos contacts pour leur dire de ne pas ouvrir les e-mails suspects envoyés depuis votre adresse.

## 🖥️ Étape 4 : Supprimer les fichiers et processus liés au ver

### ✅ 1. Vérifiez les processus actifs et supprimez ceux qui sont suspects 🕵️
- **Windows** : Ouvrez le **Gestionnaire des tâches** (**Ctrl + Shift + Échap**).
- **Mac/Linux** : Utilisez **top** ou **ps aux** pour voir les processus actifs.

Si un processus inconnu consomme beaucoup de ressources et semble suspect :
- Notez son nom et recherchez-le sur **Google** 🔎.
- Terminez le processus (**Fin de tâche** sous Windows ou **kill -9 [PID]** sous Mac/Linux).

### ✅ 2. Supprimez les fichiers malveillants 🗂️

**Windows** : Recherchez des fichiers suspects dans ces dossiers :
- `C:\Users\VotreNom\AppData\Local\Temp\`
- `C:\ProgramData\`
- `C:\Windows\System32\`

**Mac** : Regardez dans `/Library/LaunchAgents/` et `/Library/LaunchDaemons/`.

- Utilisez **Autoruns** (Windows) pour voir et supprimer les programmes qui se lancent au démarrage ([Téléchargez ici](https://docs.microsoft.com/en-us/sysinternals/downloads/autoruns)).

### ✅ 3. Vérifiez les connexions réseau suspectes 🌐
- Ouvrez l’**Invite de commande** (**Win + R** puis tapez **cmd**).
- Tapez **netstat -ano** pour voir les connexions actives.
- Si une connexion vers une adresse IP inconnue apparaît en continu, il peut s’agir du ver.

## 🔄 Étape 5 : Réinitialiser le système (si nécessaire)
➡ **Objectif** : Si le ver est trop agressif et ne peut pas être supprimé complètement.

- **Sauvegardez** vos fichiers importants 📂🔒.
- Effectuez une **réinstallation propre** de Windows ou macOS.
- **Avant de restaurer vos fichiers, analysez-les avec un antivirus** 🛡️.

## ✅ Prévention : Éviter une réinfection

✔ **Ne jamais ouvrir une pièce jointe ou un lien suspect** 📎❌.
✔ **Désactiver les macros dans les documents Office** 📄.
✔ **Mettre à jour régulièrement Windows/macOS et ses logiciels** 🔄.
✔ **Utiliser un antivirus et activer un pare-feu** 🔥.
✔ **Faire des sauvegardes régulières sur un disque externe** 📀.