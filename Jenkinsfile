pipeline {
    agent any
    stages {
        stage('git') {
            steps { 
                git credentialsId: 'github', url: 'https://github.com/praveen9177496079/gameoflife.git'
            }
        }
		stage ('build') {
		    steps {
			    sh 'mvn package'
			}
		}
		stage ('package results and test results') {
		    steps {
			    // This step should not normally be used in your script. Consult the inline help for details.
                        archive 'gameoflife-web/target/*.war'
			junit 'gameoflife-web/target/surefire-reports/*.xml'
			}
		}
    }
}

