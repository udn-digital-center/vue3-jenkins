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

         stage('NpmServe') {
                steps {
                    sh 'npm run serve'
                    
                }
            }
         stage('NpmBuild') {
                steps {
                    input message: 'Finished using the web site? (Click "Proceed" to continue)'
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