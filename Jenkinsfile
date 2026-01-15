pipeline {
    agent {
        label 'docker'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Image') {
            steps {
                
                sh 'docker build -t missionn:latest .'
            }
        }
    }

    post {
        always {
            cleanWs()
        }

        

        failure {
            mail to: 'walunjpallavi69@gmail.com',
                 subject: "Jenkins Job Failed",
                 body: "Please check the Jenkins Job"
        }
    }
}
