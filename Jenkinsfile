pipeline {
    agent {label 'devops'}

    environment {
        DOCKER_PASSWORD=credentials('DOCKER_PASSWORD')
    }

    stages {
        stage('Docker login') {
            steps {
                script {
                    sh 'echo $DOCKER_PASSWORD | docker login -u ibou1984 --password-stdin'
                }
            }
        }

        // stage('Docker build image') {
        //     steps {
        //         script {
        //             sh 'docker build -t uadb:v1.0.3 .'
        //         }
        //     }
        // }

        // stage('Docker tag image') {
        //     steps {
        //         script {
        //             sh 'docker tag uadb:v1.0.3 malicksn/uadb:v1.0.3'
        //         }
        //     }
        // }

        // stage('Docker push image') {
        //     steps {
        //         script {
        //             sh 'docker push malicksn/uadb:v1.0.3'
        //         }
        //     }
        // }
    }
}