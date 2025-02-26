pipeline {

    agent {
        docker { image 'maven' }
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