def ScriptLauncher(command) {
    bat command
}

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                ScriptLauncher('mvn clean')
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