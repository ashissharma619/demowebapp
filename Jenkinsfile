pipeline {
  agent any
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
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}
