pipeline {
    agent any
    tools{
        maven "3.9.1"
    }
    stages {
        stage('Build stage') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test stage') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy stage') {
            steps{
            script {
          deploy adapters: [tomcat9(credentialsId: 'admin', path: '', url: 'http://3.110.161.64:8080')], contextPath: null, onFailure: false, war: '**/*.war' 
        }
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
