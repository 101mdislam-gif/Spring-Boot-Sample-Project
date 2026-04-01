pipeline {
    agent any

    tools {
        jdk 'jdk11'
    }

    stages {

        stage('Check Java') {
            steps {
                sh 'java -version'
                sh 'echo $JAVA_HOME'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x mvnw'
                sh './mvnw clean package'
            }
        }
    }
}
