# 🛑 Comment détecter un Cheval de Troie sur un serveur ? 🛡🐴

Les chevaux de Troie sur un serveur sont particulièrement dangereux car ils peuvent créer des backdoors, voler des données, ou donner un accès total aux pirates.

## 🔎 Méthodes essentielles pour détecter un cheval de Troie sur un serveur Windows ou Linux

### 🔥 1. Surveiller les performances et comportements anormaux
- Utilisation excessive du CPU/RAM/disque sans raison 📊
- Connexions réseau suspectes 📱
- Fichiers modifiés ou créés récemment 💽
- Processus inconnus en arrière-plan 🔍

> **⚠️ Si votre serveur ralentit sans explication, cela peut être un signe d'infection !**

### 🧕️ 2. Vérifier les connexions réseau suspectes 🌍

Un Trojan peut établir une connexion avec un serveur distant (C&C - Command & Control).

#### ✅ Windows Server :
```powershell
netstat -ano
```
Vérifiez les connexions actives et repérez celles avec des IP suspectes.
Associez-les à des processus avec :
```powershell
tasklist /FI "PID eq [NUMERO_PID]"
```
Si un processus inconnu écoute sur un port suspect, il peut s’agir d’un cheval de Troie.

#### ✅ Linux Server :
```bash
netstat -tulnp
lsof -i
ps aux | grep [NUMERO_PID]
```
Si un processus inconnu apparaît, identifiez-le.

### 🔍 3. Vérifier les processus en cours d’exécution

#### ✅ Windows Server :
```powershell
tasklist /v
```
Cherchez des processus suspects avec des noms inhabituels (xyz123.exe).

#### ✅ Linux Server :
```bash
ps aux
ps aux | grep nom_processus
kill -9 [NUMERO_PID]
```

### 🗂 4. Vérifier les fichiers récemment modifiés

#### ✅ Windows Server :
```powershell
dir /s /od /t:w C:\
```
Vérifiez les répertoires `C:\Windows\System32` et `C:\Users\Public`.

#### ✅ Linux Server :
```bash
find / -type f -mtime -7
find / -perm -4000 -type f
```

### 🔒 5. Vérifier les tâches planifiées suspectes

#### ✅ Windows Server :
```powershell
taskschd.msc
```
Cherchez des tâches suspectes et supprimez celles inconnues.

#### ✅ Linux Server (Cron Jobs) :
```bash
crontab -l
crontab -e
```

### 🛡 6. Vérifier les clés de registre suspectes (Windows Server)
```powershell
regedit
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
```
Supprimez toute entrée suspecte.

### 🔄 7. Scanner le serveur avec un antivirus et un anti-malware

#### ✅ Windows Server :
```powershell
MpCmdRun.exe -Scan -ScanType 2
```
- Malwarebytes
- ESET Online Scanner

#### ✅ Linux Server :
```bash
apt install clamav -y
freshclam
clamscan -r /
apt install rkhunter -y
rkhunter --update
rkhunter --check
```

### 🖽 8. Supprimer le Cheval de Troie manuellement

#### ✅ Windows Server :
```powershell
taskkill /F /PID [NUMERO_PID]
del /F /Q C:\chemin\vers\virus.exe
```
Nettoyez le registre (`regedit`).

#### ✅ Linux Server :
```bash
kill -9 [NUMERO_PID]
rm -rf /chemin/du/virus
crontab -e
```

### 🚀 9. Redémarrer et sécuriser le serveur
✔ Mettez à jour votre système (`apt update && apt upgrade` ou Windows Update).
✔ Changez tous les mots de passe (surtout root/admin).
✔ Activez le pare-feu (`ufw` sur Linux, Windows Firewall).
✔ Désactivez les services inutiles (`systemctl disable service_inutile`).
✔ Vérifiez les logs (`/var/log/syslog` ou Event Viewer).