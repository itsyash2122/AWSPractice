pipeline {
    agent any
     environment {
        PATH = "$PATH:/usr/local/bin"
    }

    stages {
        stage('Creating php Image') {
            steps {
                echo 'Creating my-php image through Dockerfile in php'
         
                sh 'docker build -t my-php ./php'
                echo 'Done my-nginx Creation'
            }
        }
        
        stage('Creating nginx Image') {
            steps {
                echo 'Creating my-nginx image through Dockerfile in php'
         
                sh 'docker build -t my-nginx ./nginx'
                sh 'docker images'
                echo 'Done my-nginx Creation'
                
            }
        }
        
        
          stage('Running docker compose') {
            steps {
                echo 'Run through docker-compose.yml'
                sh 'apt-get install docker-compose'
                sh 'cd ./app'
                sh 'docker-compose build'
                sh 'docker-compose up -d'
                sh 'docker images'
                echo 'Done'
                
            }
        }
    }
    
}
