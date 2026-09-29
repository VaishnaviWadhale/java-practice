pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java code...'
                bat '"C:\\Program Files\\Java\\jdk-21\\bin\\javac" Hello.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running the program...'
                bat '"C:\\Program Files\\Java\\jdk-21\\bin\\java" Hello'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded! Everything worked.'
        }
        failure {
            echo 'Build failed! Check the console output above.'
        }
        always {
            echo 'Pipeline finished, whatever the result.'
        }
    }
}