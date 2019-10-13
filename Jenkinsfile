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
        bat "aws s3 cp target/demo-1.0.0.jar s3://${bucket}"    	
    }
}
