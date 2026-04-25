pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    environment {
        VERSION = '1.0'
    }

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true)
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
            when {
                expression { params.executeTests }
            }
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
