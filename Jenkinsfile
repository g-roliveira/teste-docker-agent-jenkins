pipeline {
    agent {
        kubernetes {
            label 'docker-dind'
        }
    }
    stages {
        stage('Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.build'
                }
            }
            steps {
                sh 'docker images'
            }
        }
    }
}
