node {

   def mvnHome

   stage('Preparation') { // for display purposes.          

      mvnHome = tool 'MAVEN_HOME'

   }

   stage('Maven Compile') {

      // Run the maven build

      withEnv(["MVN_HOME=$mvnHome"]) {

         if (isUnix()) {

            sh '"$MVN_HOME/bin/mvn" compile'

         } else {

            bat(/"%MVN_HOME%\bin\mvn" compile/)

         }

      }

   }
   stage('Unit Test') {

      // Run the maven build

      withEnv(["MVN_HOME=$mvnHome"]) {

         if (isUnix()) {

            sh '"$MVN_HOME/bin/mvn" test'

         } else {

            bat(/"%MVN_HOME%\bin\mvn" test/)

         }

      }

   }
   stage('MAven package') {

      // Run the maven build

      withEnv(["MVN_HOME=$mvnHome"]) {

         if (isUnix()) {

            sh '"$MVN_HOME/bin/mvn" package'

         } else {

            bat(/"%MVN_HOME%\bin\mvn" package/)

         }

      }

   }
}
