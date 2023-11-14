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
        stage('Test') {
            steps {
                echo 'TEST!!!'
                sh 'java -jar /usr/games/EncodingCheck_jar/EncodingCheck.jar $WORKSPACE'
            }
        }
    }
}
