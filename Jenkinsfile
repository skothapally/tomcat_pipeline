pipeline {
   agent any

  // tools {
      // Install the Maven version configured as "M3" and add it to the path. Demo comment
   //   maven "maven"
  //    jdk "java"
                
  // }

   stages {
      stage('Checkout') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/sidvijay18/tomcat_pipeline.git'   
         }

      }
      
      
     
         
          stage('Build') {
         steps {
           
        
           sh 'mvn package'
         }

      }
      
     stage(' Code Deploy') {
         steps {
        
           
          sh 'cp -rf target/test-1.0.war /opt/apache-tomcat-9.0.80/webapps'
            }

      }
   }
}
