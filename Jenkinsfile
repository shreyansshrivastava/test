pipeline {

  agent any
  
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean install'
      }
    }

    stage('Test') {
      steps {
          bat "mvn test"
      }
    }

     stage('Deploy Development') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -Pdev -DmuleDeploy'
      }
    }
    
  }
}
