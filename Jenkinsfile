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
        NAME=Ashis
        LASTNAME=Sharma
        echo $(pwd)
        echo "Hello, $NAME. Current date is $(date)" > /c/JenkinsTest/test.txt
        /c/JenkinsTest/file1.sh $NAME $LASTNAME
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