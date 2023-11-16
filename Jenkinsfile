pipeline {
    agent any
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
