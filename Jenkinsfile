pipeline {

    agent {
        label 'dynamic-agent'
    }

    stages {

        stage('Checkout') {

            steps {
                git 'https://github.com/YOUR_USERNAME/terraform-vpc-project.git'
            }
        }

        stage('Terraform Init') {

            steps {
                dir('terraform') {
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform Validate') {

            steps {
                dir('terraform') {
                    sh 'terraform validate'
                }
            }
        }

        stage('Terraform Plan') {

            steps {
                dir('terraform') {
                    sh 'terraform plan'
                }
            }
        }

        stage('Terraform Apply') {

            steps {
                dir('terraform') {
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}
