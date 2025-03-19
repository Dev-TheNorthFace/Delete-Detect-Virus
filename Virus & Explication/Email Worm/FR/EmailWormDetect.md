# 📧 Comment détecter un EmailWorm ? 🦠

Un EmailWorm est un ver informatique qui se propage par e-mail en envoyant des copies de lui-même aux contacts de la victime. Il utilise souvent des techniques d’ingénierie sociale pour inciter l’utilisateur à ouvrir une pièce jointe ou à cliquer sur un lien malveillant.

## 🚨 Signes d'infection par un EmailWorm

### 🔹 1. Réception d’e-mails suspects 📬
- Un e-mail étrange provenant d'un contact connu ou inconnu.
- Objet de message accrocheur : "Urgent!", "Facture impayée", "Vous avez gagné!", "Cliquez ici pour voir" 📢.
- Contient une pièce jointe suspecte 📎 (`.exe`, `.zip`, `.scr`, `.js`, `.vbs`, `.docm` avec macros activées).
- Un lien étrange menant à un site inconnu 🌐.
- Texte mal rédigé ou traduit automatiquement 🤔.

### 🔹 2. Vos contacts reçoivent des e-mails étranges de votre part 💌
- Des amis ou collègues signalent avoir reçu un e-mail suspect venant de vous.
- Vous voyez des e-mails envoyés que vous ne reconnaissez pas dans votre boîte "Messages envoyés" 📤.

### 🔹 3. Activité inhabituelle de votre messagerie 📊
- Connexions suspectes depuis des endroits inconnus 🌍 (vérifiez dans les paramètres de votre boîte e-mail).
- Réponses automatiques envoyées à des spams 📩.
- Votre boîte e-mail envoie massivement des messages sans votre action 📧➡️📧➡️📧.

### 🔹 4. Comportement anormal du système 🖥️
- Ralentissement du PC 📉.
- Processus suspects dans le Gestionnaire des tâches (`taskmgr.exe` sous Windows).
- Augmentation de l'utilisation du réseau 📡 (vérifiable via `netstat -ano` ou un outil comme Wireshark).

## 🔍 Comment confirmer l'infection ?

### ✅ 1. Analyse antivirus 🛡️
- Lancez une analyse complète avec un antivirus à jour (Windows Defender, Bitdefender, Malwarebytes...).

### ✅ 2. Vérifiez les paramètres de votre messagerie 🔐
- **Gmail / Outlook / Yahoo** → Vérifiez les connexions récentes et déconnectez les sessions inconnues.
- **Filtre de redirection** : Vérifiez si des règles de transfert automatique ont été ajoutées à votre insu.

### ✅ 3. Vérifiez les processus en arrière-plan 🖥️
- **Windows** : Ouvrez le Gestionnaire des tâches (`Ctrl + Shift + Échap`), regardez les processus suspects.
- **Mac/Linux** : `top` ou `ps aux` pour lister les processus actifs.

### ✅ 4. Analyse réseau 🌐
- Utilisez `netstat` (`netstat -ano`) pour voir si des connexions anormales sont ouvertes vers des serveurs inconnus.
- Installez **Wireshark** pour surveiller le trafic réseau et repérer des échanges inhabituels.

## 🛡 Comment se protéger d’un EmailWorm ?
✔ Ne jamais ouvrir une pièce jointe inconnue 📎⚠️.
✔ Ne pas cliquer sur les liens suspects 🔗🚫 (passer la souris dessus pour voir l’URL réelle).
✔ Désactiver les macros dans Word/Excel 📄❌ (*Options > Centre de gestion de la confidentialité > Paramètres des macros*).
✔ Utiliser un antivirus et le mettre à jour régulièrement 🛠️.
✔ Activer l’authentification à deux facteurs (2FA) 🔐.
✔ Changer son mot de passe e-mail en cas de doute 🔑.