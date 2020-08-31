pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'RunDevelopmentProject'
      }
    }

    stage('TX_WebTests') {
      steps {
        build 'TX_Automate_WebTest_New'
      }
    }

  }
}