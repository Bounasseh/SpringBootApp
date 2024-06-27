pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dir('D:/Carrière/Learn/Jenkins/Projects/SpringBootApp') {
                    // Construire le projet avec Maven
                    sh 'mvn clean install'
                }
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