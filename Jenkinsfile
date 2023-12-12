pipeline {
    agent any
    environment {
  name = "krishna"
}

    stages {
        stage('get info about syatem ') {
            steps {
                sh '''
                cat /etc/os-release
                cal 2023
                echo "$(currentUserGlobalRoles)"
                echo "$(name)"
                '''
            }
        }
        stage('save to file ') {
            steps {
                sh 'cat /etc/os-release > sample_file.txt'
            }
        }
        stage('get the file') {
            steps {
                sh 'ls -lrth | grep *.txt'
                sh 'pwd'
            }
        }
        stage('read the file '){
            steps  {
                sh 'cat sample_file.txt'
                
            }
            
        }
    }
}
