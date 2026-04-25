pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        VERSION = '1.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "Version is ${VERSION}"
                bat 'mvn -v'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
}
