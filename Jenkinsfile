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
                  maven -v
                '''
            }
        }
        stage('Git Test') {
            steps {
                echo "Testing Git Version"
                sh '''
                  git -version
                '''
            }
        }
        stage('SonarQube') {
            steps {
                echo 'Testing SonarQube Version'
                sh '''
                sudo systemctl status sonarqube
                '''
            }
        }
    }
}
