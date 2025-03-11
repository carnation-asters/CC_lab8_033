pipeline {   // pes1ug22am033
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output YOUR_SRN-1.cpp'  // Compile C++ file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './output'  // Run the compiled C++ program
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deployment Successful!"
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
