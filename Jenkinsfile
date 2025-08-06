pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning source code from GitHub...'
                git 'https://github.com/MonikaRGowda/tictactoejava.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java file...'
                sh 'javac tictactoe.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java program...'
                sh 'java tictactoe < input.txt'
            }
        }
    }
}
