pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        sh 'jenkins/build.bat'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
        sh 'jenkins/test-all.sh'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
        sh 'jenkins/deploy.sh'
      }
    }

  }
}
