node {

   def mvnHome

   stage('Preparation') { // for display purposes.          

      mvnHome = tool 'MAVEN_HOME'

   }

   stage('Build') {

      // Run the maven build

      withEnv(["MVN_HOME=$mvnHome"]) {

         if (isUnix()) {

            sh '"$MVN_HOME/bin/mvn" clean package'

         } else {

            bat(/"%MVN_HOME%\bin\mvn" clean package/)

         }

      }

   }
