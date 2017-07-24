pipeline {
  agent {
    node {
      label 'docker-slave'
    }
    
  }
  stages {
    stage('error') {
      steps {
        sh '''


cd flask_hello

pip3 install -r requirements.txt'''
      }
    }
    stage('Test') {
      steps {
        sh '''python3 run.py &

'''
        sh 'curl -f -L http://localhost:5555/'
      }
    }
  }
}