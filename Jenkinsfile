pipeline {
    agent {
        docker { image 'node:16-alpine' }
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone le dépôt GitHub
                git branch: 'main', url: 'https://github.com/Gazelle2022/simple_pipeline.git'
            }
        }

        stage('Test Node') {
            steps {
                sh 'node --version'
            }
        }

        stage('Hello') {
            steps {
                echo 'Hello Jenkins inside Docker!'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}

