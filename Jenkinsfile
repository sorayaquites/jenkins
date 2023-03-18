pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
                git credentialsId: 'sorayaquites', url: 'git@github.com:sorayaquites/terraform-gcp-bucket.git'
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
