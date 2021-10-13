pipeline {
    agent any       // 执行构建的节点
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