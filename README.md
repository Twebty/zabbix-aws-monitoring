🖥️ Supervision AWS avec Zabbix
📌 Description
Déploiement d'une infrastructure de monitoring centralisée sur AWS avec Zabbix conteneurisé (Docker) pour superviser un parc hybride Linux & Windows.

🏗️ Architecture
VPC : 1 sous-réseau public

EC2 :

Serveur Zabbix (t3.large, Ubuntu)

Client Linux (t3.medium, Ubuntu)

Client Windows (t3.large, Windows Server)

Docker : Conteneurs Zabbix Server + MySQL + Web UI

📁 Contenu du dépôt
Fichier/Dossier	Description
RAPPORT_TP_ZABBIX.pdf	Rapport complet du projet
/screenshots	Captures d'écran (VPC, EC2, Zabbix, etc.)
docker-compose.yml	Fichier de déploiement Zabbix
install-agent-linux.sh	Script installation agent Linux
install-agent-windows.ps1	Script installation agent Windows
🚀 Étapes rapides
Créer VPC + subnet public + Internet Gateway

Configurer Security Groups (ports 22,80,10050,10051,3389)

Lancer 3 instances EC2

Sur le serveur : docker-compose up -d

Sur les clients : installer l'agent Zabbix

Accéder à Zabbix : http://<IP_PUBLIQUE>

🔗 Accès Zabbix

Login : Admin

Mot de passe : zabbix

👩‍💻 Auteur
Najoua Mouaddab
Filière Ingénierie Informatique Big Data & IA
Encadrant : Pr. Azeddine KHIAT
Année universitaire : 2025/2026
