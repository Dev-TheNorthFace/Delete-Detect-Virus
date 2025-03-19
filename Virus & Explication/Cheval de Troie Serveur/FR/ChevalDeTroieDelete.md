# 🛑 Comment supprimer un Cheval de Troie sur un serveur ? 🛡🐴

Une fois que vous avez détecté un cheval de Troie sur votre serveur, il est crucial de le supprimer immédiatement pour éviter toute prise de contrôle par un hacker. Suivez ces étapes pour éradiquer la menace en toute sécurité !

## 🚨 1. Déconnecter le serveur d’Internet 🌐❌

🔹 **Pourquoi ?** Pour empêcher le Trojan de recevoir des commandes d’un attaquant ou d’envoyer des données volées.

### Commandes pour couper la connexion réseau :

✅ **Windows Server**  
Dans l’invite de commande (cmd.exe en admin) :

```powershell
ipconfig /release
```
Ou désactiver manuellement la carte réseau via `ncpa.cpl`.

✅ **Linux Server**  
En SSH ou en accès direct, tapez :

```bash
ifconfig eth0 down
```
Ou :

```bash
ip link set eth0 down
```
(Remplacez `eth0` par le nom de votre interface réseau.)

---

## 🔎 2. Identifier et arrêter le processus malveillant

### ✅ Windows Server
Lister les processus actifs :

```bash
tasklist /v
```

Repérer un processus inconnu (nom suspect, forte utilisation CPU/RAM).  
Tuer le processus :

```css
taskkill /F /PID [NUMERO_PID]
```

Si le Trojan revient après redémarrage, il y a une tâche planifiée ou une clé de registre suspecte (voir plus bas).

### ✅ Linux Server
Lister les processus en cours :

```bash
ps aux
```

Chercher un processus suspect :

```perl
ps aux | grep nom_processus
```

Tuer le processus :

```bash
kill -9 [NUMERO_PID]
```
Ou :

```bash
pkill -f nom_processus
```

---

## 🗑 3. Supprimer le fichier infecté

### ✅ Windows Server
Rechercher le fichier malveillant :

```bash
dir /s /od /t:w C:\
```

Supprimer le fichier infecté :

```css
del /F /Q C:\chemin\vers\virus.exe
```
Ou :

```bash
rd /S /Q C:\chemin\du\dossier\suspect
```

Vérifier dans `C:\Windows\System32` et `C:\Users\Public` s'il y a des fichiers inconnus.

### ✅ Linux Server
Chercher des fichiers récents suspectés d’être un Trojan :

```lua
find / -type f -mtime -7
```

Supprimer le fichier infecté :

```bash
rm -rf /chemin/du/virus
```
Ou :

```bash
shred -u /chemin/du/virus
```
(Utilisez `shred` si vous voulez écraser définitivement le fichier pour empêcher sa récupération.)

---

## 🔥 4. Supprimer les tâches planifiées suspectes

### ✅ Windows Server
Ouvrir le planificateur de tâches (`taskschd.msc`).  
Cherchez les tâches inconnues qui exécutent un script malveillant.  
Supprimez-les immédiatement.

### ✅ Linux Server (Cron Jobs)
Lister les tâches planifiées :

```bash
crontab -l
```

Éditer et supprimer une tâche suspecte :

```bash
crontab -e
```
(Supprimez la ligne correspondant au Trojan.)

Vérifiez également les tâches root :

```bash
cat /etc/crontab
```

---

## 🛡 5. Vérifier et nettoyer les clés de registre (Windows Server)

📌 Un Trojan peut se cacher dans le registre Windows pour se relancer après un redémarrage.

Ouvrir l’Éditeur de Registre (`regedit`).  
Aller dans ces clés :

```plaintext
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
```

Recherchez une clé inconnue qui lance un exécutable suspect.  
Supprimez l’entrée malveillante (clic droit → Supprimer).

---

## 🔍 6. Vérifier les connexions réseau suspectes

📌 Si le Trojan ouvrait une backdoor, il faut s'assurer que l'accès distant est bloqué.

### ✅ Windows Server
Lister les connexions réseau actives :

```bash
netstat -ano
```

Si une connexion suspecte apparaît, repérez son PID et tuez-le :

```css
taskkill /F /PID [NUMERO_PID]
```

Bloquez l’IP du pirate via le pare-feu :

```pgsql
netsh advfirewall firewall add rule name="Block IP Trojan" dir=in action=block remoteip=[IP_SUSPECTE]
```

### ✅ Linux Server
Lister les connexions suspectes :

```bash
netstat -tulnp
```

Tuer le processus utilisant un port suspect :

```bash
kill -9 [NUMERO_PID]
```

Bloquer l’IP du pirate avec le pare-feu `iptables` :

```css
iptables -A INPUT -s [IP_SUSPECTE] -j DROP
```

---

## 🔄 7. Redémarrer et vérifier que tout est propre

✔ **Redémarrez** le serveur et observez s’il fonctionne normalement.  
✔ **Faites un scan complet** avec un antivirus et un anti-malware.  
✔ **Regardez les logs** (`/var/log/syslog` sur Linux, `Event Viewer` sur Windows) pour vérifier qu’il n’y a plus d'activité suspecte.

---

## 🚀 8. Sécuriser le serveur pour éviter une réinfection

✔ **Mettez à jour** le serveur (`Windows Update` ou `apt update && apt upgrade`).  
✔ **Changez tous les mots de passe** (`root`, `admin`, `SSH`, `base de données`).  
✔ **Activez et configurez** le pare-feu (`ufw` sur Linux, `Windows Firewall`).  
✔ **Désactivez les services inutiles** (`systemctl disable service_inutile`).  
✔ **Utilisez un IDS** (Intrusion Detection System) comme `Fail2Ban` ou `Snort`.  
✔ **Faites des sauvegardes régulières** de vos fichiers importants.