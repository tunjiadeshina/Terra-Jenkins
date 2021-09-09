pipeline{
    agent any
    tools {
       terraform 'Terraform'
    }
    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'main', credentialsId: 'gitPT', url: 'https://github.com/tunjiadeshina/Terra-Jenkins'
            }
        }    
        stage('Terraform Init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform Apply'){
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
