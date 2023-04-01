pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/creatorshubham/java-webapp.git']]])
            }
        }
        stage('build'){
            steps{
               sh 'mvn clean package'
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
}
