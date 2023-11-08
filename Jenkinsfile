pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "currentBuild.number = ${currentBuild.number}"
				addSidebarLink(url:'https://www.cloudbess.com/', text:'CloudBess website', icon:'/userContent/cloudbees.png')
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