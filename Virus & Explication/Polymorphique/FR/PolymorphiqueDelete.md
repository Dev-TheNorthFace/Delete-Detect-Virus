# 💀 Comment supprimer un virus polymorphique de ton PC ? 💀

Les virus polymorphiques sont très difficiles à supprimer car ils changent de forme à chaque infection. Mais pas de panique ! Voici une méthode complète pour t’en débarrasser définitivement. 🔥

## 🛠 1️⃣ Déconnecte ton PC d'Internet

Certains virus polymorphiques communiquent avec un serveur distant pour télécharger de nouvelles versions d'eux-mêmes.

**Action :**
- Débranche le Wi-Fi ou le câble Ethernet pour éviter qu’il ne se mette à jour ou n’envoie des données personnelles.

## 🛠 2️⃣ Démarre en Mode Sans Échec 🔧

**Pourquoi ?** En mode sans échec, seuls les programmes essentiels de Windows sont chargés, ce qui empêche souvent le virus de s’exécuter.

### ✅ Comment faire ?
#### Sur Windows 10 & 11 :
1. Appuie sur `Shift + Redémarrer`.
2. Va dans `Dépannage → Options avancées → Paramètres de démarrage`.
3. Appuie sur `F5` pour activer `Mode sans échec avec prise en charge réseau`.

#### Sur Windows 7 & 8 :
1. Redémarre ton PC et appuie plusieurs fois sur `F8` avant que Windows ne démarre.
2. Choisis `Mode sans échec avec réseau`.

## 🛠 3️⃣ Trouve et arrête le virus en cours d’exécution

1. Ouvre le **Gestionnaire des tâches** (`Ctrl + Shift + Échap`).
2. Cherche des **processus inconnus** avec un nom bizarre (`hdsj73ks.exe`, `syswin32.dll`, etc.).
3. **Fais un clic droit** sur le processus suspect → `Ouvrir l’emplacement du fichier`.
4. Note l’endroit où il se trouve.
5. **Arrête le processus** (`Fin de tâche`).

## 🛠 4️⃣ Supprime les fichiers infectés 📂🗑️

**Cherche les fichiers suspects dans ces dossiers :**
- `C:\Users\TonNom\AppData\Roaming`
- `C:\Users\TonNom\AppData\Local\Temp`
- `C:\Windows\System32`
- `C:\ProgramData`

Si tu trouves un fichier au nom étrange (`vgh78sd.exe`, `random.dll`), **supprime-le** ! 🚀

🚨 **ATTENTION !**
Si Windows refuse de supprimer un fichier, utilise **Unlocker** pour le forcer à disparaître 💣.

## 🛠 5️⃣ Nettoie le Registre Windows 🏗️

1. Ouvre **l’Éditeur du Registre** (`Win + R` → tape `regedit`).
2. Va aux clés suivantes et supprime les entrées suspectes :
    - `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run`
    - `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`

## 🛠 6️⃣ Utilise un antivirus puissant 🔥

**Télécharge et lance un scan avec :**
- **Malwarebytes** 🦠 (le meilleur contre les malwares).
- **ESET NOD32** 🛡️ (détection heuristique avancée).
- **Kaspersky Virus Removal Tool** ⚔️ (nettoie les virus cachés).

## 🛠 7️⃣ Vérifie les programmes au démarrage 🔄

**Méthode 1 :** Ouvre `msconfig` (`Win + R` → tape `msconfig` → `Entrée`)
- Va dans l’onglet `Démarrage` 🚀.
- Décoche les programmes inconnus.

**Méthode 2 :** Utilise **Autoruns** pour voir tous les programmes au démarrage et supprimer les suspects.

## 🛠 8️⃣ Supprime les fichiers temporaires et cache 🧹

**Ouvre l’outil de nettoyage de disque :**
1. Tape `Nettoyage de disque` dans la barre de recherche Windows.
2. Sélectionne `C:` et coche `Fichiers temporaires`, `Cache`, `Corbeille`, etc.
3. Clique sur `OK` pour nettoyer !

**Alternative :** Utiliser **CCleaner** pour un nettoyage en profondeur.

## 🛠 9️⃣ Vérifie que ton PC est propre 🧐

Après toutes ces étapes :
✅ Refais un scan antivirus.
✅ Surveille ton PC pendant quelques jours.

## 🚨 🔟 Si le virus revient encore…

💀 Il est très tenace ! Voici les solutions extrêmes :

- **Live CD d’antivirus** 📀 (ex: `Kaspersky Rescue Disk`, `ESET SysRescue`).
- **Réinitialisation de Windows** (`Paramètres → Mise à jour & Sécurité → Réinitialiser ce PC`).
- **Formatage complet du disque** et réinstallation de Windows si nécessaire.

---

## 🎯 **Résumé : Comment supprimer un virus polymorphique ?**
✅ Déconnecte Internet 📡 pour éviter qu’il se mette à jour.
✅ Démarre en mode sans échec 🚀 pour empêcher le virus de s’exécuter.
✅ Arrête et supprime le processus infecté dans le Gestionnaire des tâches.
✅ Supprime les fichiers malveillants dans les dossiers système 📂.
✅ Nettoie le registre Windows 🏗️ pour éviter qu’il se relance.
✅ Fais un scan antivirus 🛡️ pour supprimer les restes du virus.
✅ Vérifie les programmes au démarrage pour éviter les infections cachées.
✅ Efface les fichiers temporaires et cache 🧹 pour un nettoyage complet.
✅ Surveille ton PC pendant quelques jours pour voir s’il reste propre.
✅ Si le virus résiste, utilise un **Live CD** ou **réinstalle Windows** 🔄.