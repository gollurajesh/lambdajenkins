def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('Build'){
        bat'mvn clean package'
    }
    stage('Push'){
        bat "aws s3 cp C:/Users/rajeshg/.jenkins/workspace/EquinoxTest/SpringEureka/target/TestEureka-0.0.1-SNAPSHOT.jar s3://${bucket}"    	
    }
}
