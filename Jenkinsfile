pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Cpt-teq/Jen-tutorials.git'
            }
        }
        stage('Build') {
            steps {
                sh '''sh Build.sh
                    echo "Build"'''
            }
        }
        stage('Deploy') {
            steps {
                sh '''sh Deploy.sh
                    echo "Deploy"'''
            }
        }
        stage('Unit') {
            steps {
                sh '''sh Unit.sh
                    echo "Unit"'''
                
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
}
