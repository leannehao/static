pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiple line shell steps work too"
          ls -lah
        '''
      }
    }
  }
}
