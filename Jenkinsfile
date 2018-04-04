pipeline {	
agent any
  stages{
    stage('Build'){
      steps {
        sh 'printenv'
        sh 'mvn clean package'	
    }
    post {
      success {
        echo 'Now Archiving...'	
        archiveArtifacts artifacts: '**/target/*.war'	
      }	
    }
  }	
  }	
}
