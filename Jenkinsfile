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
                echo 'Lancement de la construction Maven à la racine...'
                // Si ton code est dans spring_backend, on entre dedans seulement pour la commande
                sh 'cd spring_backend && mvn clean package -DskipTests'
            }
        }
    }
}