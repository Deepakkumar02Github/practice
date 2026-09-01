
pipeline {
    agent any;

    stages {

        stage('Check Windows Node') {
            steps {
                bat 'echo Hello from Jenkins'
                bat 'hostname'
                bat 'whoami'
                bat 'ver'
            }
        }

        stage('List Files') {
            steps {
                bat 'dir'
            }
        }
    }

    post {

        success {
            bat 'echo BUILD SUCCESS'
        }

        failure {
            bat 'echo BUILD FAILED'
            bat 'date /T'
        }

        always {
            bat 'echo Pipeline completed'
            bat 'ipconfig'
        }
    }
}

