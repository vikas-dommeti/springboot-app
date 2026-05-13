// pipeline {
//     agent any

//     stages {

//         stage('Build') {
//             steps {
//                 sh 'mvn clean package'
//             }
//         }

//         stage('Docker Build') {
//             steps {
//                 sh 'docker build -t springboot-app .'
//             }
//         }

//         stage('Docker Run') {
//             steps {
//                 sh 'docker run -d -p 8080:8080 springboot-app'
//             }
//         }
//         stage('Docker Run') {
//             steps {
//                 sh 'docker run -d -p 8081:8080 springboot-app'
//             }
//         }
//         stage('Docker Run') {
//             steps {
//                 sh 'docker run -d -p 8082:8080 springboot-app'
//             }
//         }
//         stage('Docker Run') {
//             steps {
//                 sh 'docker run -d -p 8083:8080 springboot-app'
//             }
//         }
//         stage('Docker Run') {
//             steps {
//                 sh 'docker run -d -p 8084:8080 springboot-app'
//             }
//         }
//     }
// }




pipeline {
    agent any

    stages {

        stage('Build Maven') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t springboot-app .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker stop springboot-container || true'
                sh 'docker rm springboot-container || true'
                sh 'docker run -d --name springboot-container -p 8081:8080 springboot-app'
            }
        }
    }
}