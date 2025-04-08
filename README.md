# Système de Gestion des Réclamations - Restaurant Management Platform 

## Vue d'ensemble
Microservice de gestion des réclamations intégré dans une plateforme de gestion de restaurant, permettant le suivi et le traitement des réclamations clients.

## Architecture Technique
- **Frontend**: Angular (port 4200)
- **Backend**: Spring Boot Microservice (port 8082)
- **Database**: MySQL 8 (port 3307)
- **Service Registry**: Eureka Server (port 8761)
- **API Gateway**: Spring Cloud Gateway (port 8081)

## Caractéristiques Principales
- Soumission et suivi des réclamations
- Notification par email automatique
- Interface admin pour la gestion
- Intégration avec le service de commandes et le service User

## Démarrage Rapide
```bash
docker-compose up -d
```

## Endpoints API
- POST /api/reclamations - Créer une réclamation
- GET /api/reclamations - Lister les réclamations
- PUT /api/reclamations/{id} - Mettre à jour une réclamation
- DELETE /api/reclamations/{id} - Supprimer une réclamation

## Configuration Email
```properties
SMTP Host: smtp.gmail.com
SMTP Port: 587
Email: Marwaniwael88@gmail.com
```

## Structure Docker
- Conteneur Frontend (Angular)
- Conteneur Backend (Spring Boot)
- Conteneur MySQL
- Conteneur Eureka
- Conteneur API Gateway

## Sécurité
- Authentification requise
- Communication inter-services sécurisée
- Validation des données entrantes

## Guide de Déploiement Git avec Submodules

### 1. Initialisation des Submodules (Première fois)
```bash
# Initialiser les submodules
git submodule init
git submodule update
```

### 2. Mise à jour des Submodules
```bash
# Pour chaque submodule (API_Gateway, Eureka-Server, Front-End, Reclamation_Service)
cd [nom-du-submodule]
git checkout master
git pull origin master
git add .
git commit -m "Update submodule: [description des changements]"
git push origin master
cd ..
```

### 3. Mise à jour du Projet Principal
```bash
# Depuis le répertoire racine
git add .
git commit -m "Update project with submodules changes"
git push origin master
```

### 4. Vérification du Statut
```bash
# Vérifier le statut des submodules
git submodule status

# Mettre à jour tous les submodules d'un coup
git submodule update --remote --merge
```

### 5. Cloner le Projet avec Submodules (Pour nouveaux développeurs)
```bash
git clone --recursive https://github.com/Application-Web-Distribution-Project/Application_Web_Distibue.git
```



## Created By AymenJallouli
