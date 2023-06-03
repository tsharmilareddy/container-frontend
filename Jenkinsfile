pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region ca-central-1 | sudo docker login --username AWS --password-stdin 778168509800.dkr.ecr.ca-central-1.amazonaws.com
            sudo docker build -t 778168509800.dkr.ecr.ca-central-1.amazonaws.com/static:latest .
            sudo docker push 778168509800.dkr.ecr.ca-central-1.amazonaws.com/static:latest
            """
        }
         }
    }
}
}
