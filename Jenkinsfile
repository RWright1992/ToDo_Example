pipeline {
    agent any

    stages {
        stage('Docker build and push') {
            steps {
                sh 'docker build -t rwright1992/todo:kubernetes .'
                sh 'docker push rwright1992/todo:kubernetes'
            }
        }
        stage('k8s deploy') {
            steps {
                sh 'kubectl apply -f cluster.yaml'
            }
        }
    }
}
