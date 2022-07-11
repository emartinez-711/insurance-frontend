pipeline {
  agent none
  stages {
    stage('Test') {
      agent { label 'nodejs-app'}
      steps {
        container('nodejs') {
          echo "Hello World"
          sh 'uname -a'
          sh 'java -version'
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
