pipeline { // pes1ug22am033
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    if (fileExists('main.cpp')) {
                        sh 'g++ -o output main.cpp'
                    } else {
                        error "Build failed: main.cpp not found!"
                    }
                }
            }
        }
        stage('Test') {
            steps {
                sh './output' // Run the compiled binary
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment successful!"
            }
        }
    }
    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
