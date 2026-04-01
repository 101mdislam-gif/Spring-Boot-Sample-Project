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
    }
}
