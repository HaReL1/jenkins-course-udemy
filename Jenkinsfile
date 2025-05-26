pipeline {
    agent any 
    tools { go 'go-1.19' }
    environment {
        ENV = "${env.BRANCH_NAME == 'master' ? 'PROD' : 'DEV'}"
    }
    stages {
        stage('build') {
            steps {
                sh './build1.sh'
            }
        }
        stage('test') {
            steps {
                sh './test1.sh'
            }
        }
    }
}
