pipeline {
    agent any
stages{
        stage('Build'){
            steps {
                sh "mvn clean package"
                sh "docker ps -a"
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}
