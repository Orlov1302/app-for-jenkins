env.MYTOOL_VERSION = '1.33'
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World!!!'
                echo "currentBuild.number = ${currentBuild.number}"
                echo "WORKSPACE = $WORKSPACE"
                echo "MYTOOL_VERSION = $MYTOOL_VERSION"
                git branch: 'main', credentialsId: '7235e8f7-b8d3-42eb-8945-32bf6657aaa3', url: 'https://github.com/Orlov1302/cod-for-jenkins.git'
                sh 'ls -a'
            }
            post {
                success {
                    script {
                        echo "currentBuild.result = ${currentBuild.result}"
                        echo "currentBuild.result = 'FAILURE'"
                        echo "currentBuild.result ---> FAILURE"
                    }
                }
            }
        }
    }
    post {
        always {
            echo "currentBuild.result = ${currentBuild.result}"
        }
    }
}
