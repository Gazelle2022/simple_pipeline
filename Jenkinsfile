pipeline {
    agent any

    triggers {
        githubPush()   
    }
//test for github webhook trigger
    stages {

        stage('push') {
            steps {
                git branch: 'main', url: 'https://github.com/Gazelle2022/simple_pipeline.git'
            }
        }
    stages {
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
}
