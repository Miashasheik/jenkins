pipeline {
    agent any

     environment {
            COURSE="jenkins"
        }
    options { 
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECONDS') 
        }
    stages {
        stage('Build') {
            steps {
               script{
                    sh """
                     echo "building"
                     echo $COURSE
                     sleep 10
                    """
               }
            }
        }
        stage('Test') {
            steps {
                 script{
                    sh """
                      echo "testing"
                    """
               }
            }
        }
        stage('Deploy') {
            steps {
              script{
                    sh """
                     echo "deploy"
                    """
               }
            }
        }
    }

     post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo "pipeline success"
        }
        failure {
            echo "pipeline failure"
        }
    }
}