pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c main/PES1UG20CS639.cpp'
                sh 'g++ -o PES1UG20CS639 main/PES1UG20CS639.cpp'
                echo 'Build successfull'
            }
        }
        stage('Test'){
            steps{
                sh './main/PES1UG20CS639'
                echo 'Test successful'
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
