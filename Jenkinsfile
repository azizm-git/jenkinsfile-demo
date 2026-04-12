pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/azizm-git/jenkinsfile-demo.git']])
                echo 'Clonage terminé ✅'
            }
        }
        stage('Build') {
            steps {
                sh 'javac Main.java'
                echo 'Compilation terminée ✅'
            }
        }
        stage('Run') {
            steps {
                sh 'java Main'
                echo 'Exécution terminée ✅'
            }
        }
    }
    post {
        success {
            echo 'Pipeline Déclaratif — Succès 🎉'
        }
        failure {
            echo 'Pipeline Déclaratif — Échec ❌'
        }
    }
}
