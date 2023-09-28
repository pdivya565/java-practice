pipeline {

    agent any

    tools {

        maven "mvn_project"
        jdk "java_home"
    }

    
    stages {
        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'pdivya565', url: 'https://github.com/pdivya565/java-practice.git']]])

                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
        stage('Build') {
            steps {
                javac App.java
            }
        }
        stage('Run') {
            steps {
                java App
            }
        }
    }
    
}
