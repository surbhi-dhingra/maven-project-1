node{
  stage('Build'){
    sh '''
    export MAVEN_HOME=/home/jenkins/maven
    printenv
    mvn clean package
    '''
    }

stage('test')
{
sh "echo Hi"
}
    
  post {
    success {
        echo 'Now Archiving...'	
        archiveArtifacts artifacts: '**/target/*.war'	
      }	
    }
  }	
  
