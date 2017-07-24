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
        sh 'python3 flask_hello/run.py &'
      }
    }
    stage('Test') {
      steps {
        sh 'curl -f -L http://localhost:5555/'
      }
    }
  }
}