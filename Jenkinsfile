pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Spygram/demo1-webapp.git'
            }
        }

        stage('Build') {
            steps {
                withMaven(maven:'maven'){
                    sh 'mvn clean package'
                }
            }
        }
    }
}