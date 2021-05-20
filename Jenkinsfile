node {

   stage('SCM') {
      // git clone
	  git 'https://github.com/praveen9177496079/gameoflife.git'
   }
   
   stage ('build the packages') {
      // mvn package
	  sh 'mvn package'
   }

   
   
   stage ('archival') {
     // archiving artifacts
	 archive 'target/*.jar'
   }

}