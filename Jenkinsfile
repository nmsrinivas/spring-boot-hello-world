pipeline {
 agent any
stages {
  stage('CodeCheckOut') {
    steps {
      script {
       checkout scm
       def mvnHome = tool 'maven-3'
       def javaHome = tool 'JAVA_1.8'
       
       }
      }
     }      
      stage('Build customer app code'){
        steps {
        script {
          try{
          sh "mvn clean install -U -Dmaven.test.skip=true"
           currentBuild.result = 'SUCCESS'
          } catch(Exception err){
          currentBuild.result = 'FAILURE'
         }
       }
      }
     }
    }
}
       
        
       
       
       
        
