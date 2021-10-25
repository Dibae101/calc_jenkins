pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '0a2c7321-5e88-497b-9ca8-3bf35dd77d58', url: 'https://github.com/Dibae101/calc_jenkins.git']]])
            }
        }
        stage('Build') {
            steps{
              git credentialsId: '0a2c7321-5e88-497b-9ca8-3bf35dd77d58', url: 'https://github.com/Dibae101/calc_jenkins.git'
              sh 'python3 calc.py'
            }
        }
        stage('Test') {
            steps {
                echo 'The Job has been tested!'
            }    
        }
    }
}
