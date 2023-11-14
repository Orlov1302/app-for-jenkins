pipeline {
    agent any

    stages {
        stage('Load') {
            steps {
                echo 'LOAD!!!'
                echo "WORKSPACE = $WORKSPACE"
                sh 'ls -a'
                git branch: 'main', credentialsId: '7235e8f7-b8d3-42eb-8945-32bf6657aaa3', url: 'https://github.com/Orlov1302/cod-for-jenkins.git'
                sh 'ls -a'
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
