pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                // Replace 'your-repo-url.git' with your GitHub repository URL
                git branch: 'main', url: 'https://github.com/snehavvv/code-with-error.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install dependencies using pip
                    sh 'pip install -r requirements.txt'
                }
            }
        }

        stage('Run Application') {
            steps {
                script {
                    // Run the Flask application
                    sh 'python app.py'
                }
            }
        }
    }
}