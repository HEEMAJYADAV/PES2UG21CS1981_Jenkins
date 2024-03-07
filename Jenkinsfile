pipeline{
  agent any
  stages{

    stages('Build'){
      steps{
        build 'PES2UG21CS198-1'
        sh 'g++ sample.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
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
