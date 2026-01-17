pipeline {
    agent {
      label 'AGENT-1'
    }

    environment {
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 1, unit: 'SECONDS')
    }

    // Build
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello Build"
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps {
                 script{
                   echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                  echo 'Deploy..'
                }
            }
        }
    }

    post {
        always{
            echo 'I will always say Hello Again!'
            deleteDir()
        }
        success {
            echo 'Hello success'
        }
        failure {
            echo 'Hello failure'
        }
    }
}