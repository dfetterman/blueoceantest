pipeline {
  agent none
  stages {
    stage('thing') {
      steps {
        parallel(
          "thing": {
            echo 'printing this message'
            
          },
          "input": {
            input(message: 'interactive input', submitter: 'danefett')
            
          }
        )
      }
    }
    stage('thing2 ') {
      steps {
        parallel(
          "thing2 ": {
            sh '''echo "shell script"
'''
            
          },
          "thing2a": {
            sh 'echo "shell script 2a"'
            
          }
        )
      }
    }
    stage('thing 3') {
      steps {
        sleep 4
      }
    }
    stage('thing 4') {
      steps {
        cleanWs(cleanWhenSuccess: true)
      }
    }
  }
}