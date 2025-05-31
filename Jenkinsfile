pipeline{
	agent any
	
	tools{
	maven='maven'
	}
	stages{
		stage('Checkout'){
		steps{
		git branch:'master',url'https://github.com/rahulreddy-25/Maven115.git'
		}
	        }
	        stage('Build'){
	        steps{
	        sh 'mvn clean package'
	        }
	        }
	        stage('Test'){
	        steps{
	        sh 'mvn test'
	        }
	        }
	        stage('Run Application'){
	        steps{
	        sh 'java -jar target/Maven115-1.0-SNAPSHOT.jar'
	        }
	        }
	       }
	post{
	  sucess{
	  	echo'Build succes'
	  	}
	  failure{
	  	echo'Build Failed'
	  	}
	  }
	 }
	 
