pipeline {
    agent any

    stages {
        stage('Build (mvn package)') {
            steps {
                echo 'Construction Maven à la racine du projet...'
                // On lance la commande directement sans le dossier spring_backend
                sh 'mvn clean package -DskipTests'
            }
        }
    }
}