pipeline {
    agent any
    
    stages {
        
        stage('Without Docker'){
            steps{
                sh 'echo "Without Docker"'
            }
        }
        
        stage('With Docker'){
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh 'echo "With Docker"'
                sh 'npm --version'
            }
        }
        
        
    }
    
}