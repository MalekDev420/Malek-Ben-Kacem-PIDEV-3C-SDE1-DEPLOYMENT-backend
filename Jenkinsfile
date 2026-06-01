pipeline {
    agent any

    stages {
        stage('Pull (Récupérer le code)') {
            steps {
                checkout scm
                echo 'Code récupéré avec succès !'
            }
        }
        
        stage('Build (mvn package)') {
            steps {
                // On demande à Jenkins d'entrer dans le dossier spring_backend pour travailler
                dir('spring_backend') {
                    echo 'Construction dans le dossier spring_backend...'
                    sh 'chmod +x mvnw'
                    sh './mvnw clean package -DskipTests'
                }
            }
        }
    }
}