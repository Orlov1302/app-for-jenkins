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
                ls -a
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
