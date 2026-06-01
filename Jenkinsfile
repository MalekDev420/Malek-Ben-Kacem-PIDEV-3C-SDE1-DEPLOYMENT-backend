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
                // On donne les droits d'exécution au fichier Maven
                sh 'chmod +x mvnw'
                // On lance la création du package (en ignorant les tests pour l'instant, car c'est une autre étape sur ton tableau)
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}