pipeline {

     agent {
        docker {
            image 'node:12-alpine'
            args '-p 3000:8080'
        }
    }
    stages {
        stage('EchoNodeVersion') {
            steps {
                sh 'node -v'
            }
        }
        stage('NpmInstall') {
            steps {
                sh 'npm i'
            }
        }
         stage('NpmBuild') {
                steps {
                    sh 'npm run build'
                }
            }
    }
    post {
        always {
            echo 'Finish!!'
        }
    }
}