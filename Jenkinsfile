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
//                sh 'npm test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'
                sh 'sudo sonar-scanner -Dsonar.host.url=http://172.31.14.184:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=cart'
            }
        }

        stage('Security Scans') {
            steps {
                echo 'Security Scans'
            }
        }

        stage('Publish Artifact') {
            when {
                expression {
                    env.TAG_NAME ==~ ".*"
                }
            }
            steps {
                echo 'Publish Artifact'
                sh 'env'
            }
        }
    }
}

