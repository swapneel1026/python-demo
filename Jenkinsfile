pipeline{
    agent any
    stages{
        stage('Create venv'){
            steps{
                sh '''
                    python3 -m venv venv
                    cd venv
                    source bin/activate
                '''
            }
        }
    }
}