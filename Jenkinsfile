pipeline {
    agent any
    stages {
      stage{
        withCredentials([
            usernamePassword(credentialsId:'github-login',usernameVariable:'USER', passwordVariable:'PASS'),
            sshUserPrivateKey(credentialsId:'ssh-key', keyFileVariable:'KEY',usernameVariable:'SSHUSER')
        ]){
            echo "Hello ${USER}"
            echo "Password: ${PASS}"
            echo "SSH Key: ${KEY}"
            echo "SSH User: ${SSHUSER}"
            
        }
      }
    }
}