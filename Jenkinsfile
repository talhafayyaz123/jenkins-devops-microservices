    // scripted

    // declarative
    pipeline {
    agent any
    //agent { docker { image  'node:20.5' } }
    stages{
        stage('Build'){
            steps{
              //  sh 'node --version'
                echo "Build"
            }
        }
        stage('Test'){
            steps{
                echo "Test"
            }
        }
        stage('Integration Test'){
            steps{
                echo "Integration Test"
            }
        }
    }
    post {
        always {
        echo 'i am awsome, i always run'
        }
        success {
        echo 'in success'
        }
        failure {
        echo 'in failure'
        }
    }
}