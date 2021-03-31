pipeline {
    agent any

    stages {
        stage('Creating php Image') {
            steps {
                echo 'Creating my-php image through Dockerfile in php'
                cd php
                docker build -t my-php .
                echo 'Done my-php'
            }
        }
    }
}
