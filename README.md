# Système de Prédiction des Admissions Cinéma 🎬

Ce projet est un système complet de prédiction des entrées en salle de cinéma, combinant la collecte de données, l'analyse prédictive et une interface web.

## 📁 Structure du Projet

- `data_collection/` : Scripts et configurations pour la collecte automatisée des données
  - Spiders Scrapy pour la collecte des données box-office
  - Configuration Airflow pour l'automatisation
  - Scripts d'installation ODBC
  
- `model/` : Modèles de prédiction et expérimentations
  - Intégration avec Azure ML
  
- `web_app/` : Interface utilisateur web
  - Système d'authentification
  - Visualisation des prédictions

- `docker-compose.yaml` : Configuration Docker pour le déploiement

## 🚀 Installation

1. Cloner le repository :
```bash
git clone https://github.com/jeremy-vangansberg/simplon-cinema-admission-prediction.git
cd cinema-admission-prediction
```

2. Configuration de l'environnement :
```bash
# Installation des dépendances pour la collecte de données
cd data_collection
pip install -r requirements.txt

# Démarrage des services Docker
docker-compose up -d
```

3. Configuration d'Airflow :
```bash
cd data_collection
./deploy_airflow.sh
```

## 🔧 Configuration

- Créer un fichier `.env` dans le dossier `data_collection/`
- Configurer les accès à la base de données et les API keys nécessaires
- Ajuster les paramètres dans `airflow.cfg` selon vos besoins

## 🏃‍♂️ Utilisation

1. Collecte des données :
   - Les DAGs Airflow orchestrent la collecte automatique
   - Accès à l'interface Airflow : http://localhost:8080

2. Interface Web :
   - Démarrer l'application web : `cd web_app && [commandes de démarrage]`
   - Accès : http://localhost:[PORT]

## 🤝 Contribution

- Fork le projet
- Créer une branche pour votre fonctionnalité
- Soumettre une Pull Request
