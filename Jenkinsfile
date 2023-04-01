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
    }
//     post{
//         success{
//             mail to: "shubhamc2211@gmail.com",
//             subject: "Build is successfull",
//             body: "success"
//         }
//     failure{
//       mail to: "shubhamc2211@gmail.com",
//             subject: "Build is failed",
//             body: "failed"
//     }
//   }
}
