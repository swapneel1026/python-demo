pipeline{
    agent any
    stages{
        stage('Create venv'){
            steps{
                sh '''
                    python3 -m venv venv
                '''
            }
        }
        stage('Install Dependecies'){
            steps{
                sh '''
                    venv/bin/pip install -r requirements.txt
                '''
            }
        }
        stage('Run Tests'){
            steps{
                sh '''
                 venv/bin/python3 -m pytest --junitxml=report.xml
                '''
            }
        }
        stage('Publish Test Reports'){
            steps{
                junit 'report.xml'
            }
        }
    }
    post{
        always{
            echo 'Pipline Finished'
        }
    }
}