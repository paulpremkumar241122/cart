pipeline {

    agent { node { label 'workstation' } }
    options {
        ansiColor('xterm')
    }

    stages {

        stage('Code Built') {
            steps {
                sh 'npm install'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Unit Test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'
            }
        }

        stage('Security Scans') {
            steps {
                echo 'Security Scans'
            }
        }

        stage('Publish Artifact') {
            steps {
                echo 'Publish Artifact'
            }
        }
    }
}
