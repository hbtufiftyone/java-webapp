pipeline {
  agent any
  tools {
    maven 
  }
  stages {
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage ('Testing') {
      steps {
      sh 'mvn test' 
        }
    }
  }
    post{
        success{
            mail to: "shubhamc2211@gmail.com",
            subject: "Build is successfull",
            body: "success"
        }
    failure{
      mail to: "shubhamc2211@gmail.com",
            subject: "Build is failed",
            body: "failed"
    }
  }
}
