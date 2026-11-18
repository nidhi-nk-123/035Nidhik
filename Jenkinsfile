pipeline {
  agent any

  stages {
    stages('Build') {
      steps {
        bat 'docker --version && docker build -t labhome
      }
    }
    stage('Run') {
      steps {
          bat 'docker run -d --name labhome-con -p 8082:80 labhome'
      }
    }
    stage('Deploy') {
      steps {
        bat 'docker ps'
      }
    }
  }
}
