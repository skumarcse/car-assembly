pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'rm -rf build'
                sh 'mkdir build'
                sh 'touch build/car.txt'
                sh 'echo engine > build/car.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'grep "engine" build/car.txt'
            }
        }
        stage('Publish') {
            steps {
                archiveArtifacts artifacts: 'build/'
            }
        }
    }
}
