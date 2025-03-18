pipeline {
  agent any
  stages {
    stage('Clone Repository'){
      steps{
        checkout([$class: 'GitSCM',
        branches: [[name: '*/main']],
        userRemoteConfigs: [[url: 'https://github.com/anirudhpk01/PES1UG22CS093_Jenkins']]])
      }
    }
    stage('Build'){
      steps{
        build 'PES1UG22CS093-1'
        sh 'g++ hello_again.cpp -o -output'
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
  
