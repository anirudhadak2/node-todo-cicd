pipeline {
    agent any

    stages{
        stage('Code'){
            steps {
                git url: 'https://github.com/Akanksha2619/node-todo-cicd.git', branch: 'master'
            }
        }
        stage('Build and Test'){
            steps {
                sh 'docker build . -t node-todo-app-cicd:latest' 
            }
        }


        stage('Deploy'){
            steps {
                sh 'docker-compose down && docker-compose up -d'
            }
        }

        stage('Successfully Deployed'){
            steps {
                echo "node-to-do app has been successfully deployed"
            }
        }   
    }
}
