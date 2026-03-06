pipeline {
    agent {label 'AGENT-1'}

    environment {
        BUCKET_NAME = "sumit-devops-static-site-2026"
    }

    stages {

        stage('Deploy to S3') {
            steps {
                sh '''
                echo "Deploying website to S3..."
                aws s3 sync . s3://$BUCKET_NAME --delete
                '''
            }
        }

    }
}
