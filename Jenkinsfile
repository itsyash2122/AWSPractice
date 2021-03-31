pipeline {
    agent any

    stages {
        stage('Creating php Image') {
            steps {
                echo 'Creating my-php image through Dockerfile in php'
                sh 'cd php'
                sh 'docker build -t my-php .'
                echo 'Done my-php'
            }
        }
    }
}
