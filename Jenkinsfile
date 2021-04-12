pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
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
        stage('Unit and Int Test') {
            parallel {
                stage('Unit Test') {
                                     steps { 
                                                echo 'Running Unit Tests ....'
                                     }
                 stage('Int Test') {
                     agent {  
                         docker {
                                    reuseNode false
                                    image 'ubuntu'
                                }
                            }
                     steps {
                         echo 'Running Int Tests ...'
                     }
        }
     }
        stage('Pause For Confirmation') {
            steps { 
                    input("Do You Want To Proceed To Prod ?")
                   
            }
        }
        stage('Prod') {
            steps {
                echo 'Hello Prod You Are Done !!!'
                echo "${params.Greeting} World!"
            }
        }
    }
}   
    }
}
