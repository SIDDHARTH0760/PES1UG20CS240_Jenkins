pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS240-1', wait: false
                 ec 'Build by CS240 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS240 successful
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS240 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
