pipeline {
    agent none
    tools{
        maven "3.9.1"
    }
    stages {
        stage('Test stage') {
            agent any
            steps {
                sh 'mvn test'
            }
        }
    }
    post{
        success{
            mail to: "ska78657@gmail.com",
            subject: "Build is successfull",
            body: "success"
        }
    failure{
      mail to: "ska78657@gmail.com",
            subject: "Build is failed",
            body: "failed"
    }
  }
}
