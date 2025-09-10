// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/yourusername/your-repo-name.git'
            }
        }

        stage('Deploy to Apache') {
            steps {
                script {
                    def deployDir = '/var/www/html/login-app'

                    // Clean deploy folder and copy new files
                    sh """
                        sudo mkdir -p ${deployDir}
                        sudo rm -rf ${deployDir}/*
                        sudo cp -r * ${deployDir}
                    """
                }
            }
        }
    }
}
