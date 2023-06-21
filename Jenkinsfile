pipeline {
    agent {
        label 'docker'
    }
    stages {
        stage("verify tooling") {
            steps {
                script {
                    docker.image('docker').inside('-u root') {
                        sh '''
                            docker ps
                        '''
                    }
                }
            }
        }
    }
}
