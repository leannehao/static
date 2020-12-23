pipeline {
  agent any
  stages {
    stage ('Lint HTML') {
      steps {
        sh "tidy -q -e *.html"
      }
    }
    stage ('Upload to AWS') {
      steps {
        sh 'echo "Hello World"'
        withAWS(region:'us-east-2', credentials:'aws-static') {
          s3Upload(file:'index.html', bucket:'jenkinss3leanne', path:'index.html')
        }        
        sh '''
          echo "Multiple line shell steps work too"
          ls -lah
        '''
      }
    }
  }
}
