# ansible-config-mgt

Change Made
Elastic IP
ansible-config-artifact

# Jenkins File for Quick Task

pipeline {
    agent any

  stages {
    stage('Initial Cleanup') {
      steps {
        dir ("${WORKSPACE}") {
          deleteDir()
        }
      }
    }

    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }

    stage('Package') {
      steps {
        script {
          sh 'echo "Package Stage"'
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          sh 'echo "Deploy Stage"'
        }
      }
    }

    stage('Cleanup') {
      steps {
        cleanWs()
        }
      }
    }

    }
