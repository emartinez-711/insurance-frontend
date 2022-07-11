pipeline {
  agent none
  stages {

    stage('Say Hello from default container') {
    agent { label 'nodejs-app' }      
      steps {
        echo 'Hello World!'   
        sh 'java -version'
        sh 'uname -a'
        sh 'pwd'        
      }
    }
    
    stage('Test') {
      agent { label 'nodejs-app'}
      steps {
        container('nodejs') {
          echo "Hello World, using echo and not sh echo"
          sh 'uname -a'
          sh 'pwd'
        }
      }
    }
    
  }
}
