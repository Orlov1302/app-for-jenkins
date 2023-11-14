pipeline {
    agent any

    stages {
        stage('Load') {
            steps {
                echo 'LOAD!!!'
                echo "WORKSPACE = $WORKSPACE"
                sh 'ls -a'
                git branch: 'main', url: 'https://github.com/Orlov1302/cod-for-jenkins.git'
                sh 'ls -a'
            }
        }
        stage ('Input') {
            steps {
                script {
                    env.RESP1 = input message: '<message>', parameters: [string(defaultValue: '', description: 'Enter response 1', name: 'RESPONSE1')]
                    env.RESP2 = input message: '<message>', parameters: [string(defaultValue: '', description: 'Enter response 2', name: 'RESPONSE2')]
                    echo "${env.RESP1}"
                }
                echo "${env.RESP2}"
            }
        }
        stage('Test') {
            steps {
                echo 'TEST!!!'
                sh 'java -jar /usr/games/EncodingCheck_jar/EncodingCheck.jar $WORKSPACE'
            }
        }
    }
}
