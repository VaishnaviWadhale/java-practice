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
}