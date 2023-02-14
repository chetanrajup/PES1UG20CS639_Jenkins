pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS639.cpp'
                sh 'g++ -o PES1UG20CS639 PES1UG20CS639.cpp'
                echo 'Build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS639'
                echo 'Test stage successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline failed'
        }
    }
}
