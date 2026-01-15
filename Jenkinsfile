pipeline {
    agent {
        label 'docker'
    }

    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
    }

    post {
        always {
            cleanWs()
        }

        success {
            mail to: 'walunjpallavi69@gmail.com',
                 subject: "Jenkins Job Success",
                 body: "Jenkins Job is Successful"
        }

        failure {
            mail to: 'walunjpallavi69@gmail.com',
                 subject: "Jenkins Job Failed",
                 body: "Please check the Jenkins Job"
        }
    }
}
