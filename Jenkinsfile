pipeline{
    agent{label 'rishi12'}
    stages{
        stage('docker'){
            steps{
                sh 'cd /kub/kub/ && docker image build -t 90188/music:latest && docker image push 90188/music:latest' 
            }
        }
        stage('Deploy'){
            sh 'cd /kub/kub/ && kubectl apply -f k8s-deploy.yml'
            }
        }
    }

