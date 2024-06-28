pipeline {
        agent any
        stages {
            stage('Build') {
                steps {
                    script {
                        // Choisissez la commande en fonction de votre script
                        sh 'sudo apt install pip'
                        sh 'pip install pandas' // Installer les dépendances
                        sh 'python data_analysis.py' // Exécuter le script Python
                    }
                }
            }
        }
    }