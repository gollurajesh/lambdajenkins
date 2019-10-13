def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'

pipeline { 
    agent any  
	environment {
    	PATH = "C:\Program Files\Git\bin;C:\Program Files\Git\usr\bin;$PATH",
    	JAVA_HOME = "C:\Program Files\Java\jdk1.8.0_161"
  	}
    stages { 
    	
        stage('Build') { 
            steps {
            		echo "PATH is: $PATH"
	                bat'mvn clean compile'
	        }
	        
        }
        
    }
}