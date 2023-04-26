pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:Jayachandra-2/nodejs-sample-application.git'
            }
        }
        stage('node') {
            steps {
              sh 'sudo yum install nodejs -y'
            }
        }
        stage('npm') {
            steps {
              sh 'npm start'
            }
        }
        //  stage('nvm') {
        //     steps {
        //       sh '. ~/.nvm/nvm.sh'
        //     }
        // }
        //  stage('nvm1') {
        //     steps {
        //       sh 'npm install'
        //     }
        // }
    }
}