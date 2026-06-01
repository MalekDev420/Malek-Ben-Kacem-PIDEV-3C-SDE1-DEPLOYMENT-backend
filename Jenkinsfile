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
                dir('spring_backend') {
                    echo '--- LISTE DES FICHIERS ---'
                    sh 'ls -la' // <--- C'est la commande magique
                    echo '--------------------------'
                    
                    sh 'chmod +x mvnw'
                    sh './mvnw clean package -DskipTests'
                }
            }
        }