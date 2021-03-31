def setupVirtualEnv() {
    sh echo 'What A beautiful World'
    sh 'printenv'
}
pipeline {
    agent any
    environment {
        NEW_VERSION = '1.3.4.5'
    }

    stages {
        stage('Setup environment') {
            steps {
                setupVirtualEnv()
                setupRightsizing()
            }
        }
        stage('test') {
            steps {
                echo 'Hello test'
                echo "building version ${NEW_VERSION}"
            }
        }
       stage('UAT') {
            steps {
                echo 'Hello UAT'
            }
        }
        stage('Prod') {
            steps {
                echo 'Hello Prod You Are Done !!!'
            }
        }
    }
}
