pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
                git credentialsId: 'a1763fab-b819-4fce-a712-44e04b9609d1', url: 'https://github.com/revanthsai-bandi/terraform-with-gcp.git'
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
