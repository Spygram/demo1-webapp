pipeline{
  agent any
  stages{
    stage('checkout'){
      steps{
        git 'https://github.com/Spygram/demo1-webapp.git'
      }
    }
    stage('build'){
      sh "mvn clean package"
    }
  }
}
