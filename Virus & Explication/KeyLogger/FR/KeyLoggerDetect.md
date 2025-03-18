## 1️⃣ Vérifier les processus en cours

📌 Un keylogger fonctionne généralement en arrière-plan.

➡️ Ouvre le Gestionnaire des tâches (`Ctrl + Shift + Échap`) et cherche :
- Des processus inconnus ou suspects.
- Un programme qui consomme peu de CPU mais tourne en permanence.
- Un processus avec un nom générique (`WindowsUpdate.exe`, `svchost.exe` hors de son dossier d’origine).

💡 **Outil recommandé** : [Process Explorer (de Microsoft)](https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer) → Il permet de voir les détails des processus et leur emplacement.

---

## 2️⃣ Vérifier les programmes au démarrage

📌 Les keyloggers cherchent à se relancer automatiquement.

➡️ Tape `msconfig` dans **Exécuter** (`Win + R`), puis :
- Va dans l’onglet **Démarrage** et cherche des programmes suspects.
- Désactive ceux que tu ne connais pas.

💡 **Outil recommandé** : [Autoruns (de Microsoft)](https://docs.microsoft.com/en-us/sysinternals/downloads/autoruns) → Il affiche **TOUTES** les applications qui se lancent au démarrage.

---

## 3️⃣ Vérifier les connexions réseau

📌 Certains keyloggers envoient les frappes à un serveur distant.

➡️ Utilise la commande suivante dans **PowerShell** :
```powershell
netstat -ano
```
Si tu vois des connexions inconnues ou vers une IP externe suspecte, c’est louche.

💡 **Outil recommandé** : [Wireshark](https://www.wireshark.org/) → Permet de surveiller tout le trafic réseau en détail.

---

## 4️⃣ Vérifier les fichiers suspects

📌 Les keyloggers enregistrent souvent les frappes dans un fichier texte caché.

➡️ Cherche des fichiers étranges dans ces dossiers :
- `C:\Users\[ton_user]\AppData\Roaming\`
- `C:\Windows\System32\`
- `C:\Users\Public\`

💡 **Outil recommandé** : [Everything](https://www.voidtools.com/) → Recherche instantanément tous les fichiers cachés.

---

## 5️⃣ Scanner avec un antivirus / antimalware

📌 Un bon antivirus détecte la majorité des keyloggers connus.

➡️ Utilise :
- **Windows Defender** (avec une analyse approfondie).
- **Malwarebytes** (spécialisé en logiciels espions).
- **HitmanPro** (scan cloud avancé).

---

## 6️⃣ Vérifier les hooks clavier

📌 Certains keyloggers utilisent des “hooks” pour intercepter les frappes clavier.

➡️ Tape cette commande dans **PowerShell en mode administrateur** :
```powershell
Get-WinEvent -LogName Microsoft-Windows-Security-Auditing | Select-String "Hook"
```
Si ça renvoie un résultat, il peut y avoir un keylogger actif.

💡 **Outil recommandé** : [SpyShelter](https://www.spyshelter.com/) → Il détecte les hooks clavier en temps réel.

---

## 7️⃣ Redémarrer en mode sans échec

📌 Les logiciels malveillants sont souvent désactivés en mode sans échec.

➡️ **Démarre en Mode sans échec avec prise en charge réseau** (`F8` au démarrage ou via `msconfig`).

Si le keylogger ne fonctionne plus = il est bien installé sur le système.

---

## 8️⃣ Vérifier les permissions des applications

📌 Certains keyloggers demandent l’accès au clavier.

➡️ Sur **Windows 10/11** :
- **Paramètres** → **Confidentialité & Sécurité** → **Saisie au clavier**.
- Regarde quelles applications ont accès aux frappes clavier.

---

## 💡 **Si tu trouves un keylogger** :
✅ Déconnecte-toi immédiatement d’Internet (évite que tes frappes soient envoyées).
✅ Désinstalle le logiciel malveillant (**via Programmes & fonctionnalités**).
✅ Supprime les fichiers suspects (**AppData, System32**).
✅ Scanne ton PC avec un **antivirus + Malwarebytes**.
✅ **Change tous tes mots de passe** (depuis un autre appareil sûr).