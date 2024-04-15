pipeline {
    agent any

    stages {
        stage("Clone") {
            steps {
                sh 'echo 1'
                git branch: 'main', url: 'https://github.com/Vivek0624/cicd-react-jenkins.git'
                sh 'echo 2'
            }
        }
        stage("Install") {
            steps {
                sh 'echo 3'
                sh 'pwd'
                sh 'npm i'
                sh 'echo 4'
            }
        }
        stage("Build") {
            steps {
                sh 'echo 5'
                sh 'sudo npm run build'
                sh 'echo 6'
            }
        }
        stage("Deploy") {
            steps {
                sh 'echo 7'
                sh 'sudo rm -rf /var/www/html/*'
                sh 'sudo cp -r dist/* /var/www/html'
                sh 'echo 8'
            }
        }
    }
}
