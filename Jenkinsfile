pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES2UG21CS360-1'
        sh 'g++ main.cpp -o output'

      }
    }
    stage('Test'){
      steps{
      sh './invalid_output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
}
}