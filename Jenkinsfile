pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'RunDevelopmentProject'
      }
    }

    stage('TX_WebTests') {
      parallel {
        stage('TX_WebTests') {
          steps {
            build 'TX_Automate_WebTest_New'
          }
        }

        stage('TX_APITests') {
          steps {
            build 'TX_Automate_APITest_New'
          }
        }

        stage('TX_MobileTests') {
          steps {
            build 'TX_Automate_MobileTest_New'
          }
        }

        stage('Performance') {
          steps {
            build 'Performance'
          }
        }

      }
    }

  }
}