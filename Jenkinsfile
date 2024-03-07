pipeline{
  agent any
  stages{
//      stage('Clone repository'){
//        steps{
//          checkout([$class: 'GitSCM',
//          branches:[[name: '*/main']],
 //         userRemoteConfigs:[[url:]]])
//}
//}
    stages('Build'){
      steps{
        build 'PES2UG21CS198-1'
        sh 'g++ main.cpp -o output'
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
