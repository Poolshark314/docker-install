pipeline {
    agent any
    stages {
        stage('install docker') {
            steps {
                sh 'sudo apt update'
                sh 'sudo apt install -y apt-transport-https ca-certificates curl software-properties-common'
                sh 'curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -'
                sh 'sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"'
                sh 'sudo apt update'
                sh 'apt-cache policy docker-ce'
                sh 'sudo apt install -y docker-ce'
                sh 'sudo systemctl status docker'
                sh 'sudo usermod -aG docker ${USER}'
            }
        }
    }
}