pipeline {	
agent any
  stages{
    stage('Build'){
      steps {
        env.MAVEN_HOME = '/home/jenkins/maven'
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
