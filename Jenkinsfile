pipeline {
    agent{
        label 'docker'
    }
    stages {

        stage ('checkout') {
            steps {
                checkout scm
            }
        }
    }

    post {
        always {
            cleanWs ()
        }
    }
}