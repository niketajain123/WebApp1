pipeline {
  agent { label 'build-node' }
  stages {
    stage('Build') {
      steps {
        sh 'ecgo "Building..."'
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