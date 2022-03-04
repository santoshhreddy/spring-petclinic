pipeline {
  agent any 
  stages{
    stage ('checkout code from github') {
      steps{
        git ' '
      }
    }
    stage ('build the code with maven') {
      steps{
        sh 'mvn clean package'
      }
    }
    stage('archive artifacts') {
      steps{
        archiveArtifacts 'target/*.jar'
      }
    }
    stage ('junit test reports') {
      steps{
        junit 'target/surefire-reports/*.xml'
      }
    }
  }
}

  
