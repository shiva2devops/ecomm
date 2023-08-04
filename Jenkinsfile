pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/shiva2devops/ecomm.git'
            }
        }
        stage('build docker image') {
            steps {
                sh 'docker rmi -f mshiva7396/ecommapp:latest'
                sh 'docker build -t mshiva7396/ecommapp .'
                
            }
        }
        stage('Run docker container') {
            steps {
                sh 'docker container run -dt -p 9000:80 mshiva7396/ecommapp'
            }
            }
        }
    }

