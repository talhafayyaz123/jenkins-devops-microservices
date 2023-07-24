    // scripted

    // declarative
    pipeline {
    stages{
    stage('Build'){
        steps{
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
     always(){
      echo 'i am awsome, i always run'
     }
      success(){
      echo 'in success'
     }
      failure(){
      echo 'in failure'
     }
    }
}