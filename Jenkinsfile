pipeline {
  agent {
    node {
      label 'docker-slave'
    }
    
  }
  stages {
    stage('') {
      steps {
        sh 'pip3 install -r flask_hello/requirements.txt'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Test": {
            sh '''python3 run.py &

'''
            
          },
          "": {
            sh 'curl -f -L http://localhost:5555/'
            
          }
        )
      }
    }
  }
}