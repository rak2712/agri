pipeline {
    agent any

    stages {
        stage('Deploy to Apache') {
            steps {
                script {
                    def deployDir = '/var/www/html/login-app'

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
