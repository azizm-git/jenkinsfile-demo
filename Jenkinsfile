node {
    try {
        stage('Clone') {
            checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/azizm-git/jenkinsfile-demo.git']])
            echo 'Clonage terminé ✅'
        }
        stage('Build') {
            sh 'javac Main.java'
            echo 'Compilation terminée ✅'
        }
        stage('Run') {
            sh 'java Main'
            echo 'Exécution terminée ✅'
        }
    } catch(err) {
        echo 'Erreur dans le pipeline ❌'
        throw err
    } finally {
        echo 'Fin du pipeline (toujours exécuté)'
    }
}
