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
    stage('Test') {
        when {
            expression { return true }
        }
        steps {
            echo 'Testing..'
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
  

}
