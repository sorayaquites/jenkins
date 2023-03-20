pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
                git credentialsId: 'fc92a882-3bd3-4c51-b920-233cc14a9a04', url: 'git@github.com:sorayaquites/terraform-gcp-bucket.git ', branch: 'main'
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
