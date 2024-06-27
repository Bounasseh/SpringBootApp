pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Cloner le dépôt
                git 'https://github.com/Bounasseh/SpringBootApp'
            }
        }
        stage('Build') {
            steps {
                // Construire le projet avec Maven
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Le build a réussi!'
        }
        failure {
            echo 'Le build a échoué.'
        }
    }
}