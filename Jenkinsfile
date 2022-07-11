pipeline {
  agent none
  stages {
    stage('Test') {
      agent { label 'nodejs-app'}
      steps {
        container('nodejs') {
          echo 'Hello World'
          echo '$(uname -a)'
          sh 'java -version'
          sh 'uname -a'
        }
      }
    }
    stage('Say Hello from default container') {
    agent { label 'nodejs-app' }      
      steps {
        echo 'Hello World!'   
        sh 'java -version'
      }
    }
  }
}
