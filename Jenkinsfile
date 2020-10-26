pipeline {
    agent any
    options {
        timeout(time: 1, unit: 'HOURS') 
        skipStagesAfterUnstable()
        disableConcurrentBuilds()
    }
    environment {
        JENKINS_USER_ID = "${sh(script: 'id -u', returnStdout: true).trim()}"
        JENKINS_GROUP_ID = "${sh(script: 'id -g', returnStdout: true).trim()}"
    }

  }
  stage('Build') {
            agent {
                dockerfile {
                    additionalBuildArgs "--build-arg DOCKER_HOST_USER_ID=${env.JENKINS_USER_ID} --build-arg DOCKER_HOST_USER_GROUP_ID=${env.JENKINS_GROUP_ID}"
                    reuseNode true
                }
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