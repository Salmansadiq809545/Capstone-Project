pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
                git url:'https://github.com/Salmansadiq809545/Capstone-Project'
            }
        }
        
        stage('Build Image') {
            steps {
                sh 'docker build -t reactimage .'
                sh 'docker tag reactimage:latest akshu20791/dev:latest'
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                   sh 'docker run -itd --name My-first-container -p 3000:3000 akshu20791/dev:latest'
                    
                }
            }
        }
    }
}
