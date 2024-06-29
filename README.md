# Composants du Projet
Ce projet démontre la mise en place d'un pipeline de données automatisé utilisant Jenkins et GitHub. Il illustre comment exécuter automatiquement des analyses de données en réponse à des modifications de code, renforçant ainsi les pratiques d'intégration et de déploiement continus (CI/CD) dans un contexte d'analyse de données.

# Composants du Projet
1- Script Python d'Analyse de Données (data_analysis.py) :
Lit les données de ventes à partir d'un fichier CSV
Calcule et affiche des statistiques de base (total des ventes, moyenne, maximum, minimum)
2- Données d'Exemple (sales_data.csv) :
Fichier CSV contenant des données de ventes simulées pour tester le script
3- Pipeline Jenkins (Jenkinsfile) :
Définit les étapes d'exécution du pipeline
Installe les dépendances nécessaires (pandas)
Exécute le script d'analyse de données

# Fonctionnalités
Intégration GitHub-Jenkins pour le déclenchement automatique du pipeline
Exécution automatique de l'analyse de données à chaque modification du code
Affichage des résultats d'analyse dans la console Jenkins

# Configuration
Le dépôt GitHub contient le code source et les données d'exemple
Jenkins est configuré pour surveiller le dépôt GitHub
Le pipeline Jenkins s'exécute automatiquement lors des modifications du code

# Utilisation
Clonez ce dépôt
Modifiez le script Python ou les données CSV selon vos besoins
Poussez vos modifications sur GitHub
Observez l'exécution automatique du pipeline dans Jenkins

