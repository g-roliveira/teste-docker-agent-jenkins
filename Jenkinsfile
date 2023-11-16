pipeline {
    agent {
        // Define o agente Docker com a label "docker-dind"
        dockerfile {
            label 'docker-dind'
            filename 'Dockerfile'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    stages {
        stage('Build') {
            steps {
                // Comandos para construir seu projeto
                sh 'docker build -t meu-projeto .'
            }
        }

        stage('Test') {
            steps {
                // Comandos para testar seu projeto
                sh 'docker run meu-projeto ./run-tests.sh'
            }
        }

        stage('Deploy') {
            steps {
                // Comandos para implantar seu projeto
                sh 'docker run meu-projeto ./deploy.sh'
            }
        }
    }
}
