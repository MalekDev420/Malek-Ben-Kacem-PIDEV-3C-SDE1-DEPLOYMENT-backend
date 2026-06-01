pipeline {
    agent any

    stages {
        stage('Build (mvn package)') {
            steps {
                echo 'Construction Maven à la racine du projet...'
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                // Utilise le nom 'SonarQube' configuré dans Gérer Jenkins > Configurer le système
                withSonarQubeEnv('SonarQube') {
                    // Remplace 'backend-projet' par la clé exacte que tu as créée dans SonarQube
                    sh 'mvn sonar:sonar -Dsonar.projectKey=backend-projet'
                }
            }
        }
    }

    post {
        always {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}