pipeline{
  agent any
  stages{
    stage('checkout'){
      steps{
        git 'https://github.com/Spygram/demo1-webapp.git'
      }
    }
    stage('build'){
      steps{
        sh "mvn clean package"
    }
      }
  }
}
