pipeline {
    agent any

    stages {
        stage('Pull (Récupérer le code)') {
            steps {
                // Cette commande dit à Jenkins de télécharger le code depuis GitHub
                checkout scm
                echo 'Code récupéré avec succès !'
            }
        }
        
        stage('Build (mvn package)') {
            steps {
                // On simule la construction du projet pour vérifier que la connexion marche
                echo 'Création du package Maven en cours...'
                // sh './mvnw clean package' (On activera cette vraie commande juste après !)
            }
        }
    }
}