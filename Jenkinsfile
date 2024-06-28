// pipeline {
//         agent any
//         stages {
//             stage('Build') {
//                 steps {
//                     script {
//                         // Choisissez la commande en fonction de votre script

//                         sh 'pip install pandas' // Installer les dépendances
//                         sh 'python data_analysis.py' // Exécuter le script Python
//                     }
//                 }
//             }
//         }
//     }

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/aochi22/jenkins-data-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        withEnv([
                            "PYTHON_HOME=/usr/bin",
                            "PATH=${env.PATH}:${env.PYTHON_HOME}"
                        ]) {
                            sh 'echo "Running on Unix"'
                            sh 'pip install pandas' // Installer les dépendances
                            sh 'python3 data_analysis.py' // Exécuter le script Python
                        }
                    } else {
                        withEnv([
                            "PYTHON_HOME=C:\\Users\\rochi\\AppData\\Local\\Microsoft\\WindowsApps",
                            "PATH=${env.PATH};${env.PYTHON_HOME}"
                        ]) {
                            bat 'echo "Running on Windows"'
                            bat 'pip install pandas' // Installer les dépendances
                            bat 'python data_analysis.py' // Exécuter le script Python
                        }
                    }
                }
            }
        }
    }
}
