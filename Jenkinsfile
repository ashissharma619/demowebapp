pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        sh 'jenkins/build.sh'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}
