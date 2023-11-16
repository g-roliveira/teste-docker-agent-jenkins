pipeline {
    agent {
        label 'docker-dddddddd'
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
