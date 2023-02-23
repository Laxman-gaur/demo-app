pipeline {
    agent any
    stages {
        stage('git clone') {
            steps {
                sh 'cd /var/lib/jenkins/workspace'
                sh 'git clone https://github.com/Laxman-gaur/demo-app.git'
                sh 'cd ./demo-app'
                sh 'pwd'
            }
        }
        stage('install the dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('deploy to production') {
            steps {
                sh 'pm2 start app.js'
            }
        }
    }
}
