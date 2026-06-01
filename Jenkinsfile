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
                echo 'Lancement de la construction Maven...'
                // On s'assure que le fichier est exécutable
                sh 'chmod +x mvnw'
                // On lance la construction
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}