pipeline {
    agent {
        label "dockerworker"
    }
    stages {
        stage('Build image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
        stage('Run app') {
            steps {
                sh 'docker run -p my-app'
            }
        }
    }
    post {
        always {
            deleteDir()
        }
    }
}
