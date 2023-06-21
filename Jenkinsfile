pipeline {
    agent any
    stages {
        stage("Pull Changes") {
            steps {
                dir("/var/jenkins_home/app/jenkins-test") {
                    git branch: 'master', url: 'https://github.com/omarhosny206/jenkins-test.git'
                }
            }
        }
      
       stage("Run Docker Compose") {
            steps {
                sh "docker compose -f /var/jenkins_home/app/jenkins-test/docker-compose.yml up -d --build"
            }
        }
    }
}
