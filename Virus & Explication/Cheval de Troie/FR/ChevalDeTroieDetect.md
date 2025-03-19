# 🚫 Comment détecter un Cheval de Troie ? 🦠🐴

Un Cheval de Troie (Trojan) est un logiciel malveillant qui se fait passer pour un programme légitime pour infecter votre ordinateur. Il peut inclure des portes dérobées (backdoors) qui permettent aux pirates d’avoir un accès distant à votre système sans votre consentement.

🚨 **Détecter un Cheval de Troie rapidement est crucial pour éviter des pertes de données et empêcher un pirate de prendre le contrôle de votre machine !** 🚨

## 🔍 Signes d’infection par un Cheval de Troie

### 🔹 1. Performances anormales du système 🖥️🐌
- Votre PC devient très lent sans raison apparente.
- Vos ventilateurs tournent fort même sans applications ouvertes.
- Votre PC s’éteint ou redémarre tout seul.

### 🔹 2. Activité réseau inhabituelle 📱🔍
- Votre connexion Internet est lente alors que vous n’utilisez rien de lourd.
- Vous remarquez des pics de trafic dans votre gestionnaire de réseau.
- Un programme inconnu essaie de se connecter à Internet.

**🔎 Vérification rapide :**

**Sur Windows** : Ouvrez l’Invite de commande (cmd.exe) et tapez :
```bash
netstat -ano
```
🤔 Regardez si des connexions suspectes sont actives.

**Sur Mac/Linux** : Tapez :
```bash
lsof -i
```
🤔 Vérifiez les connexions réseau suspectes.

### 🔹 3. Apparition de nouveaux programmes inconnus 🗑️
- Des applications que vous n’avez jamais installées apparaissent sur votre PC.
- Des pop-ups étranges s’affichent sans raison.
- Vous remarquez des extensions de navigateur que vous n’avez pas ajoutées.

### 🔹 4. Comportement suspect de l’antivirus ou du pare-feu 🛡️❌
- Votre antivirus se désactive tout seul.
- Votre pare-feu Windows est désactivé sans votre intervention.
- Vous ne pouvez plus ouvrir le gestionnaire des tâches (`Ctrl + Shift + Échap`).

### 🔹 5. Modifications étranges dans Windows ⚠️
- De nouveaux utilisateurs inconnus sont créés sur votre PC.
- Certains fichiers système sont modifiés.
- Vous voyez des processus suspects en arrière-plan.

**🔎 Vérification rapide :**
- Ouvrez le **Gestionnaire des tâches** (`Ctrl + Shift + Échap`) et recherchez des processus étranges avec des noms aléatoires (`xyz123.exe`).
- Tapez `tasklist` dans l’Invite de commande (`cmd.exe`) pour voir tous les processus actifs.

## 🧐 Comment confirmer la présence d’un Cheval de Troie ?

### ✅ 1. Analyser avec un antivirus ou un anti-malware 🛡️
- Utilisez **Windows Defender, Malwarebytes, Bitdefender, Kaspersky...**
- Faites un **scan complet du système**, pas seulement un scan rapide !

### ✅ 2. Vérifier les programmes qui se lancent au démarrage 🚀
- Tapez **`msconfig`** dans la barre de recherche Windows.
- Allez dans l’onglet **Démarrage** et regardez si des programmes inconnus se lancent au démarrage.

### ✅ 3. Vérifier les tâches planifiées 🕒
- Tapez **`taskschd.msc`** pour ouvrir le **Planificateur de tâches**.
- Supprimez les tâches inconnues qui pourraient exécuter le cheval de Troie en arrière-plan.

### ✅ 4. Vérifier les clés de registre suspectes 🗝️
- Tapez **`regedit`** dans la barre de recherche Windows.
- Allez dans :
```bash
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
```
- Supprimez les entrées suspectes qui exécutent des fichiers inconnus au démarrage.

### ✅ 5. Vérifier les connexions réseau suspectes 🌐
- Tapez **`netstat -ano`** pour voir les adresses IP auxquelles votre PC est connecté.
- Si une connexion inconnue est active en permanence, il se peut qu’un pirate ait un accès distant à votre machine.

---

En suivant ces étapes, vous pourrez repérer un Cheval de Troie avant qu'il ne cause trop de dégâts. Si vous en détectez un, passez immédiatement à la suppression et renforcez la sécurité de votre système ! ✨