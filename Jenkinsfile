pipeline {
  agent {
    node {
      label 'docker-slave'
    }
    
  }
  stages {
    stage('error') {
      steps {
        sh 'pip3 install -r flask_hello/requirements.txt'
      }
    }
    stage('Test') {
      steps {
        sh '''python3 flask_hello/run.py &
'''
        sh 'curl -f -I http://localhost:5555/'
      }
    }
  }
}