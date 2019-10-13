def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'

pipeline { 
    agent any 
    stages { 
    	
        stage('Build') { 
            steps {
	                bat'mvn clean compile'
	        }
	        
        }
        stage('Push'){
        	sh "aws s3 cp C:/Users/rajeshg/.jenkins/workspace/EquinoxTest/SpringEureka/target/TestEureka-0.0.1-SNAPSHOT.jar s3://${bucket}"
    	}
        
    }
}