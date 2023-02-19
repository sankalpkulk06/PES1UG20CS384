pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gcc hello.cpp -o hello.exe'
        echo 'Build Stage successful'
        }
    }
    stage('Test') {
      steps {
        sh 'hello.exe'
        echo 'Test Stage successful'
        post {
          always {
            junit 'target/surefire-reports/*.xml'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh ''
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
