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
}