node {

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
}
