pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                echo 'Building'
                sh 'g++ -o PES1UG21CS481 main/hello.cpp'
            }
            post {
                failure {
                    echo 'Pipeline failed during the build stage'
                }
            }
        }
        
        stage('Test') {
            steps {
                // Print output of .cpp file using a shell script

                //non existing file
                echo 'testing'
                sh './PES1UG21CS367'
            }
            post {
                failure {
                    echo 'Pipeline failed during the test stage'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here, if applicable
                echo 'deploying'
            }
            post {
                failure {
                    echo 'Pipeline failed during the deploy stage'
                }
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
    }
}
