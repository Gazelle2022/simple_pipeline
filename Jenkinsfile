pipeline {
    agent any
    triggers { githubPush() }

    stages {
        stage('Checkout') {
            steps {
                // Clone le repo
                git branch: 'main', url: 'https://github.com/Gazelle2022/simple_pipeline.git'
            }
        }

        stage('Hello') {
            steps {
                echo 'Hello Jenkins!'
            }
        }

        stage('Test Build') {
            steps {
                echo 'This is a simple pipeline test.'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
