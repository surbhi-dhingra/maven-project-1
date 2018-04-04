pipeline {	
agent any
  stages{
    stage('Build'){
      steps {
        sh 'printenv'
        env.MAVEN_HOME = '/home/jenkins/maven'
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
