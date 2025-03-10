pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh '''
                    g++ -o YOUR_SRN-1 main.cpp
                    echo "Build completed successfully"
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh '''
                    ./YOUR_SRN-1
                    echo "Testing completed successfully"
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh '''
                    echo "Deployment completed successfully"
                '''
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
