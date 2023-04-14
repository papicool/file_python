pipeline {
    agent {
        dockerfile {
           filename 'dockerfile'
        }
    }
    stages {
        stage('Checkout') {
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/solbarre/file_python.git'
                    sh "ls -lart ./*"
                }
            }
        }
        stage('exe') {
            steps{
                sh 'python fibonacci.py'
            }
            
        }
    }
    
}
