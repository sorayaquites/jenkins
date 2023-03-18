pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
                git credentialsId: '0066e554-f818-4114-913d-cb99c5acfe72', url: 'https://github.com/sorayaquites/jenkins.git'
            }
        }
        stage('Initialize'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Plan'){
            steps{
                sh 'terraform plan'
            }
        }
        stage('Apply'){
            steps{
                sh 'terraform apply -auto-approve'
            }
        }
    }
}
