node {
    stage('Clone') {
        checkout scm
        echo 'Clonage du projet terminé'
    }

    stage('Build') {
        sh 'javac Main.java'
    }

    stage('Run') {
        sh 'java Main'
    }
}
