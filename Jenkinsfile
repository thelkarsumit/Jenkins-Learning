pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Maven Test') {
            steps {
                echo "Testing Maven Version"
                sh '''
                echo "maven -v"
                '''
            }
        }
        stage('Git Test') {
            steps {
                echo "Testing Git Version"
                sh '''
                echo "Testing is done"
                '''
            }
        }
        stage('SonarQube') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff"
                '''
            }
        }
    }
}
