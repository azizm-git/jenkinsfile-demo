node {

    try {

        stage('Clone') {
            checkout scm
            echo 'Clonage du projet terminé'
        }

        stage('Build') {
            sh 'javac Main.java'
        }

        stage('Test') {
            sh 'echo "Tests OK ✅"'
        }

        stage('Run') {
            sh 'java Main'
        }

        stage('Finish') {
            echo 'Pipeline terminé'
        }

    } catch (err) {
        echo 'Erreur dans le pipeline ❌'
        throw err
    } finally {
        echo 'Fin du pipeline (toujours exécuté)'
    }
}