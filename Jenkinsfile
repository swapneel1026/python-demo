pipeline{
    agent any
    stages{
        stage('Create venv'){
            steps{
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                '''
            }
        }
        stage('Install Dependecies'){
            steps{
                sh '''
                    pip install -r requirements.txt
                '''
            }
        }
    }
}