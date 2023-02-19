pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ sankalp.cpp -o sankalp'
        build job: 'PES1UG20CS384', wait: false
        echo 'Build Stage successful'
        }
    }
    stage('Test') {
      steps {
        sh 'cat sankalp.cpp'
        echo 'Test Stage successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment successful'
       }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
