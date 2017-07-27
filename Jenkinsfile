pipeline {
  agent {
    node {
      label 'docker-slave'
    }
    
  }
  stages {
    stage('error') {
      steps {
        sh 'git clone https://github.com/tbenlulu/flask_hello.git'
        sh 'pip3 install -r flask_hello/requirements.txt'
      }
    }
    stage('Test') {
      steps {
        sh '''python3 flask_hello/run.py &
'''
        sh 'curl -f -I http://127.0.0.1:5555/'
      }
    }
  }
}