pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path. Demo comment
      maven "maven"
      jdk "java"
                
   }

   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/sidvijay18/tomcat_pipeline.git'

            // Run Maven on a Unix agent.
            //sh "mvn -Dmaven.test.failure.ignore=true clean package"

            // To run Maven on a Windows agent, use
           bat "mvn package"
         }

      }
      
      stage('Deployment') {
         steps {
        
            // To run Maven on a Windows agent, use
           bat "copy /Y target\tomcat-1.0.war E:\apache-tomcat-9.0.16-windows-x64\apache-tomcat-9.0.16\webapps"
         }

      }
   }
}
