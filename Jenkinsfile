pipeline {

	agent {
		label 'test'
	}
	stages{   
		
		stage(install){
			steps{
				    sh 'mvn clean install'
			     
			}
			post{
			    always{
			        archiveArtifacts artifacts: 'target/**.jar', followSymlinks: false
			    }
			}
		}
		stage ('clean ws'){
	        steps {
	            cleanWs()
	        }
	    }
	}
}

