pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'sudo pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest test_app.py'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '*.py', fingerprint: true
            }
        }
    }
}

