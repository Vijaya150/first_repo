pipeline {
    agent any
    stages {

        stage('Print Parameter'){
            steps{
                echo "User accepted branch: ${params.Branch_name}"
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        echo 'Running Unit Tests...'
                    }
                }
                stage('Integration Tests') {
                    steps {
                        echo 'Running Integration Tests...'
                    }
                }
                stage('Security Tests') {
                    steps {
                        echo 'Running Security Tests...'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}

