## 🔎 Comment détecter un Ransomware ? 🦠💰

Un ransomware est un logiciel malveillant qui chiffre vos fichiers et exige une rançon pour les récupérer. Il utilise généralement des algorithmes puissants comme AES (Advanced Encryption Standard) et RSA (Rivest-Shamir-Adleman) pour verrouiller les données.

🚨 **Plus vite vous le détectez, plus vous avez de chances de limiter les dégâts !** 🚨

---

### ⚠️ Signes d’infection par un ransomware

#### 🔹 1. Vos fichiers sont renommés ou deviennent inaccessibles 📂🔒
- Les fichiers ont une nouvelle extension inconnue (`.locked`, `.encrypted`, `.cryp1`, `.ransom`, `.locky`, etc.).
- Impossible d’ouvrir vos documents, images ou vidéos, même avec le bon logiciel.
- Des messages d’erreur s’affichent en indiquant que le fichier est corrompu ou chiffré.

#### 🔹 2. Un message de rançon s’affiche 💰💻
- Un fichier texte ou une fenêtre apparaît avec un message du type :
  > *Vos fichiers ont été chiffrés. Payez XXX Bitcoins pour les récupérer.*
- Les ransomwares célèbres affichent souvent un **compte à rebours** ⏳ pour forcer la victime à payer rapidement.

#### 🔹 3. L’ordinateur devient lent et se comporte anormalement 🖥️🐌
- Disque dur ou processeur **surchargé** sans raison.
- Activité réseau élevée 📡, surtout vers des **serveurs inconnus**.
- Fichiers qui **disparaissent** ou qui **changent de taille** soudainement.

#### 🔹 4. Un antivirus ou un outil de sécurité est désactivé 🛡️❌
- Certains ransomwares **désactivent votre antivirus** ou votre pare-feu Windows.
- **Windows Defender est désactivé** sans raison.

#### 🔹 5. Programmes et processus suspects en arrière-plan 🕵️‍♂️
- Ouvrez le **Gestionnaire des tâches** (`Ctrl + Shift + Échap` sous Windows) et recherchez des processus inconnus consommant beaucoup de ressources.
- **Commande utile :**
  ```powershell
  tasklist | findstr /i ransomware
  ```
- Utilisez **Autoruns** (outil Microsoft) pour voir les applications qui se lancent au démarrage ([Télécharger ici](https://docs.microsoft.com/en-us/sysinternals/downloads/autoruns)).

#### 🔹 6. Connexions suspectes vers des adresses IP inconnues 🌍
- **Commande utile :**
  ```cmd
  netstat -ano
  ```
- Si vous voyez une **adresse IP suspecte** qui maintient une connexion persistante, cela pourrait être un ransomware communiquant avec son serveur.

---

### 🔍 Comment confirmer la présence d’un ransomware ?

#### ✅ 1. Analyse avec un antivirus ou un anti-malware 🛡️
- Lancez un scan complet avec **Malwarebytes, Windows Defender, Kaspersky, Bitdefender, ESET**...

#### ✅ 2. Vérification des extensions de fichiers modifiées 🗂️
- Si tous vos fichiers ont une **nouvelle extension inconnue**, c'est un signe clair d’infection.

  **Exemple :**
  ```plaintext
  document.docx -> document.locked
  photo.jpg -> photo.encrypted
  ```
- **Outils de détection :**
  - [ID Ransomware](https://id-ransomware.malwarehunterteam.com/) pour identifier le type de ransomware à partir des fichiers chiffrés.

#### ✅ 3. Vérification des clés de registre Windows 🗝️
- Certains ransomwares ajoutent des entrées dans le registre Windows :
  - Ouvrez **l’Éditeur du Registre** (`Win + R` puis tapez `regedit`).
  - Allez dans :
    ```plaintext
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
    ```
  - Si vous voyez une **entrée suspecte** qui exécute un programme inconnu au démarrage, c’est un indicateur d’infection.

#### ✅ 4. Analyse du trafic réseau 🌐
- Utilisez **Wireshark** ou **GlassWire** pour voir si votre PC envoie des données à des serveurs inconnus.
- Si une **connexion active envoie des données en continu** vers une adresse IP étrangère, méfiez-vous !

---

## 🚨 Que faire si vous êtes infecté ? 🚨

❌ **NE PAYEZ PAS LA RANÇON !** 💰🚫
> Il n’y a aucune garantie que vous récupérerez vos fichiers.

### 🔥 Étapes d’urgence

1️⃣ **Déconnectez immédiatement** votre PC du réseau (**Wi-Fi + Ethernet**) pour empêcher la propagation.
2️⃣ **Éteignez l’ordinateur** et redémarrez en **mode sans échec** pour tenter de le nettoyer.
3️⃣ **Analysez et supprimez le ransomware** avec un antivirus ou un outil dédié (*ex: Malwarebytes Anti-Ransomware*).
4️⃣ **Tentez de restaurer vos fichiers** via des sauvegardes ou des outils de déchiffrement gratuits.