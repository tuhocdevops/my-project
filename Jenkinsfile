pipeline{
   agent any
   tools{
       maven 'maven_3_9_4'
   }
   stages{
      stage('sonar quality check'){
        step{
            withSonarQubeEnv(credentialsId: 'sonar-token') 
            sh 'mvn clean package sonar:sonar'
        }
      }
   }
}