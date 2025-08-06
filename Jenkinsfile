pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning source code from GitHub...'
                git 'https://github.com/MonikaRGowda/tictactoecicid.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java file...'
                bat 'javac tictactoe.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java program...'
                bat 'java tictactoe < input.txt'
            }
        }
    }
}


