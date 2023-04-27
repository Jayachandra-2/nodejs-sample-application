pipeline {
  agent any

  stages {
    stage('Clone repository') {
      steps {
        git branch: 'main', url: 'git@github.com:Jayachandra-2/nodejs-sample-application.git'
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Build application') {
      steps {
        sh 'npm run build'
      }
    }

    stage('Deploy application') {
      steps {
        sh 'cp -R build/* /var/www/html'
        sh 'sudo service httpd restart'
      }
    }
  }

//   post {
//     always {
//       sh 'npm run test'
//     }
//   }
}
