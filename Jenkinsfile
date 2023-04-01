pipeline {
    agent none
    tools{
        maven '3.9.1'
    }
    stages {
        stage('Test stage') {
            agent any
            steps {
                sh 'mvn test'
            }
        }
    }
}
