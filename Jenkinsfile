pipeline {
  agent any

  stages {

    stage('Checkout') {
      steps {
        git 'https://github.com/101mdislam-gif/Spring-Boot-Sample-Project.git'
      }
    }

    stage('Build') {
      steps {
        sh 'chmod +x mvnw'
        sh './mvnw clean package'
      }
    }

    stage('Run App') {
      steps {
        sh '''
        nohup java -jar target/*.jar > app.log 2>&1 &
        sleep 15
        curl http://localhost:8080 || true
        '''
      }
    }
  }
}
