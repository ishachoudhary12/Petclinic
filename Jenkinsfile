pipeline {
    agent any
    
    tools{
        jdk 'JAVA'
        maven 'Maven-3.6.3'
    }

    stages {
        stage('GIT Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests=true'
            }
        }
    }
}
     
     
