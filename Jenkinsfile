pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/pdivya565/java-practice.git'
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
