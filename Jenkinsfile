    // scripted

    // declarative
    pipeline {
    //agent any
     agent { docker { image  'maven:3.6.3' } }
    stages{
    /* stage('Build'){
        steps{
            sh 'mvn --version'
            echo "Build"
        }
     } */

       stage('Build'){
        withMaven(maven: 'mvn') {
            sh "mvn clean package"
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