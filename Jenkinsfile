pipeline {

    agent {
        docker { image 'maven:3.8.1-adoptopenjdk-11' }
      }

    stages {
        stage('Build') {
            steps {
                echo 'Start Clean pacakge'
                sh 'mvn -B -DskipTests clean package'
                echo 'End Clean pacakge'
            }
        }
        stage('Test') {
            steps {
                echo 'Start Test'
                sh 'mvn test'
                echo 'End Test'
            }
        }
    }
}