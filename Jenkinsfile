pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Hello Test'
            }
        }
        stage('UAT') {
            steps {
                echo 'Hello UAT'
            }
        }
        stage('Prod') {
            steps {
                echo 'Hello Prod'
            }
        }
        post{
            always {
                echo "Build Completed"
            }
        }
    }
}
