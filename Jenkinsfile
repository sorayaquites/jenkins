pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
                git credentialsId: 'a5e42587-a21e-4f59-9207-260c4d882c34', url: 'git@github.com:sorayaquites/terraform-gcp-bucket.git', branch: 'master'
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
