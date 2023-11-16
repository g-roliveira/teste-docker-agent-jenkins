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
                    registryUrl 'https://harbor-dev.gustavo.com/docker-hub'
                    registryCredentialsId 'harbor'
                    reuseNode true
                }
            }
            steps {
                sh 'build-app'
            }
        }
    }
}
