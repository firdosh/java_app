pipeline {
    agent any
    environment {
        NEW_VERSION = '1.3.4.5'
    }

    stages {
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
