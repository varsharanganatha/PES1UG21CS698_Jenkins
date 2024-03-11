 pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is Build stage."
                build 'PES1UG21CS698-1'
                sh 'g++ ./main/hello.cpp -o output'
                echo "Build Stage Successful"
            }
        }
        stage('Test') { 
            steps {
                ec "This is Test stage." 
                s './output'
                echo "Test Stage Successful"
            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy stage."
                echo "Deployment Success"
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}
