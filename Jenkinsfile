pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo building...'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Running tests..."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying app..."'
        input message: "wanna deploy", ok: "Merge"
      }
    }
  }
  post {
    success {
      echo 'Build succeeded!'
    }
    failure {
      echo 'Build failed!'
    }
  }
}