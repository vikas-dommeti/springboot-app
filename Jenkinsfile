pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t springboot-app .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker run -d -p 8080:8080 springboot-app'
            }
        }
        stage('Docker Run') {
            steps {
                sh 'docker run -d -p 8081:8080 springboot-app'
            }
        }
        stage('Docker Run') {
            steps {
                sh 'docker run -d -p 8082:8080 springboot-app'
            }
        }
        stage('Docker Run') {
            steps {
                sh 'docker run -d -p 8083:8080 springboot-app'
            }
        }
        stage('Docker Run') {
            steps {
                sh 'docker run -d -p 8084:8080 springboot-app'
            }
        }
    }
}