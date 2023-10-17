ipeline {
    agent any 
    environment {
    DOCKERHUB_CREDENTIALS = credentials('lubnaibrahimmu-dockerhub')
    }
    stages { 
        stage('SCM Checkout') {
            steps{
            git 'https://github.com/LubnaIbrahimMU/Jobathon.git'
            }
        }

        stage('Build docker image') {
            steps {  
                sh 'docker build -t lubnaibrahimmu/flask-app:$BUILD_NUMBER ./MySQL-and-Python/FlaskApp'
                sh 'docker build -t lubnaibrahimmu/mysql-db:$BUILD_NUMBER ./MySQL-and-Python/MySQL_Queries'
            }
        }
        stage('login to dockerhub') {
            steps{
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }
        stage('push image') {
            steps{
                sh 'docker push lubnaibrahimmu/flask-app:$BUILD_NUMBER'
                sh 'docker push lubnaibrahimmu/mysql-db:$BUILD_NUMBER'

            }
        }
}
post {
        always {
            sh 'docker logout'
        }
    }
}