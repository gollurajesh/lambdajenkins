def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'

pipeline { 
    agent any 
    environment {
	  PATH = "C:/Program Files/Git/bin;C:/Program Files/Git/usr/bin:${env.PATH}"
	}
    stages { 
    	
        stage('Build') { 
            steps {
            		echo "PATH is: $PATH"
	                bat'mvn clean compile'
	        }
	        
        }
        stage('Push'){
        	steps {
        		bat "aws s3 cp C:/Users/rajeshg/.jenkins/workspace/EquinoxTest/SpringEureka/target/TestEureka-0.0.1-SNAPSHOT.jar s3://${bucket}"
        	}
        	
    	}
        
    }
}