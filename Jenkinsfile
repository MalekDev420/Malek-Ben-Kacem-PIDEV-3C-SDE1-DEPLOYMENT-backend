pipeline {
    agent any

    stages {
        stage('Pull') {
            steps {
                checkout scm
                echo 'Code récupéré avec succès !'
            }
        }
        
        stage('Build (mvn package)') {
            steps {
                dir('spring_backend') {
                    echo '--- Diagnostic : Liste des fichiers ---'
                    sh 'ls -la' 
                    echo '--- Lancement de la construction Maven ---'
                    // On utilise 'mvn' directement pour éviter le problème du fichier ./mvnw manquant
                    sh 'mvn clean package -DskipTests'
                }
            }
        }
    }
}