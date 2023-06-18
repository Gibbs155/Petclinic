pipeline {
    agent any
    
    tools{
        jdk 'jdk112'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Gibbs155/Petclinic.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn clean"
            }
        }
        
        stage('Build') {
            steps {
               sh "mvn package -DskipTests=true"
            }
        }
        
        
        
        
    }
}
