pipeline {
    agent { label 'AGENT-1' }
    environment{
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello, This is build"
                        echo "Project: $PROJECT"
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Hello, This is test"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                 script{
                    sh """
                        echo "Hello, this is deploy"
                    """
                }
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
         failure { 
            echo 'Build is failed!'
        }
         success { 
            echo 'Build is success!'
        }
    }
}