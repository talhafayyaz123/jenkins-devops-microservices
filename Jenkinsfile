    // scripted

    // declarative
    pipeline {
    agent any
    //agent { docker { image  'maven:3.9.3' } }
    environment{
     dockerHome=tool 'MyDocker'
     mavenHome=tool 'MyMaven'
     PATH="$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages{
        stage('Checkout'){
            steps{
                sh 'mvn --version'
                sh 'docker --version'
                echo "Build"
                echo "$PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
            }
        }
            stage('Complie'){
                steps{
                    sh 'mvn clean compile'
                }
        }
        stage('Test'){
            steps{
               sh "mvn test"
            }
        }
        stage('Integration Test'){
            steps{
                sh "mvn failsafe:integration-test failsafe:verify"
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