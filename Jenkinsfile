pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        echo $(pwd)
        /c/JenkinsTest/file12.sh
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