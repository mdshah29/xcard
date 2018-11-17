<<<<<<< HEAD
node('maven-label'){
 stage("preparation"){
  sh "echo Hello world"
 }
 stage("preparation"){
  sh "echo Hello world"
 }
 stage("preparation"){
  sh "echo Hello world"
 }

=======

node('maven-label') {
   def mvnHome
   stage('Preparation') { // for display purposes
     
     git branch: 'master', url: 'https://github.com/retail-1/xcard.git'
         
      mvnHome = tool 'maven'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
   }
>>>>>>> 83fb31a9603f966ae2a0c25d5b1f12099081bfb2
}
