pipeline {
    agent {
        // Define o agente Docker com a label "docker-dind"
        label 'docker-dind'
    }

    stages {
        stage('Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.build'
                }
            }
            steps {
                sh 'build-app'
            }
        }
    }
}
