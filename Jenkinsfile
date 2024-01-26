pipeline {
    agent {
        label 'vm-1'
    }
    
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/rakeshsguttedar/BoardgameListingWebApp.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn compile"
                echo "hello"
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
        
        stage('Install') {
            steps {
                sh "mvn install"
            }
        }
    }
}
