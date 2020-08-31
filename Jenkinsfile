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
        sh '''d:
cd C:\\Users\\Automation\\Desktop\\TX_Automate_New\\cucumber-jvm-template-master-2.0_New_Updated
mvn test -Dcucumber.options="--tags @Amazon"'''
      }
    }

  }
}