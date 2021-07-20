pipeline {

  agent any
  environment {
    //adding a comment for the commit test
    //DEPLOY_CREDS = credentials('deploy-anypoint-user')
    MULE_VERSION = '4.3.0'
    BG = "<BUSINESS-GROUP>"
    WORKER = "Micro"
  }
  stages {
    stage('Build') {
      steps {
            sh 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          sh "mvn test"
      }
    }

     
  }

  tools {
    maven 'M3'
  }
}