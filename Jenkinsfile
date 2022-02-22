pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                
              checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github', url: 'https://github.com/sandeepdevops2022/mobile.git']]])  
                
            }
        }
        
        
        stage('build') {
            steps {
               sh 'ls'
            }
        }
        
        
        stage('deploy') {
            steps {
                script {
                    sh '''
                cd /home/ec2-user/
              sh add.sh sandeep
              '''
                }
            }
        }
    }
}
