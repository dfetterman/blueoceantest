pipeline {
  agent none
  stages {
    stage('stage 1') {
      steps {
        sh 'echo "stage 1"'
      }
    }
    stage('stage 2') {
      steps {
        waitUntil() {
          input(message: 'interactive input goes here', ok: 'true', submitter: 'danefett')
          echo 'foobar is my message'
        }
        
      }
    }
    stage('') {
      steps {
        error '1'
      }
    }
  }
}