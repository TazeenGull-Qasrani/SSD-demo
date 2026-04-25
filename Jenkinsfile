pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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

    agent any

    environment {
        VERSION = '1.0'
    }

    stages {
        stage('Build') {
            steps {
                echo "Version is ${VERSION}"
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
    }
  

}
