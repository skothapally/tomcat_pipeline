pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path. Demo comment
      maven "maven"
      jdk "java"
                
   }

   stages {
      stage('Code Checkout') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/sidvijay18/tomcat_pipeline.git'   
         }

      }
      
      
      stage('Unit Testing') {
         steps {
           
            // To run Maven on a Windows agent, use
           bat "mvn test"
         }
      }
         
          stage('Build') {
         steps {
           
            // To run Maven on a Windows agent, use
           bat "mvn package"
         }

      }
   }
}
