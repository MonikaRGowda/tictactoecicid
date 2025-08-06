pipeline {
    agent any

    tools {
        jdk 'Java17'
    }
    
     stages {
        stage('Checkout') {
            steps {
                echo 'Cloning source code from GitHub...'
                git branch: 'main', url: 'https://github.com/MonikaRGowda/tictactoecicid.git'
            }
        }

        stage('Build') {
    steps {
        echo 'Checking Java setup in Jenkins...'
        bat 'where java'
        bat 'where javac'
        bat 'java -version'
        bat 'javac -version'

        echo 'Listing files in workspace...'
        bat 'dir'

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





