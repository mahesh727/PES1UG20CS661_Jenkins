pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
          sh 'g++ -o PES1UG20CS661 PES1UG20CS661_Mahesh.cpp'
          build job: 'PES1UG20CS661-1'
      }
    }
    
    stage('Test') {
      steps {
        sh './PES1UG20CS661'
      }
    }
    
    stage('Deploy') {
      steps {
          echo 'Success'
      }
    }
  }
  
  post {
    failure {
      echo "Pipeline failed!!.."
    }
  }
}
