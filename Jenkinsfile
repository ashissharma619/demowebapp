pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        sh 'jenkin/build.sh'
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