pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh '''
                export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
                export PATH=$JAVA_HOME/bin:$PATH

                java -version

                chmod +x mvnw
                ./mvnw clean package
                '''
            }
        }

        stage('Docker Build') {
    steps {
        sh '''
        docker build -t your-dockerhub-username/bankapp:latest .
        '''
            }
      }
    }
}
