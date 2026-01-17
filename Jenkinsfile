pipeline {
    agent {
      label 'AGENT-1'
    }

    // Build
    stages {
        stage('Build') {
            steps {
                script{
                  echo 'Building'
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