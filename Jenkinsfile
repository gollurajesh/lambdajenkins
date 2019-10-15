def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'
def jarfilename = 'demo-1.0.0.jar'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('Build'){
        bat "mvn clean install -Dversion=lambdajenkins${BUILD_NUMBER}"
    }
    stage('Push'){
        bat "aws s3 cp target/lambdajenkins${BUILD_NUMBER} s3://${bucket}"    	
    }
    stage('Deploy'){
        bat "aws lambda update-function-code --function-name ${functionName} --s3-bucket ${bucket} --s3-key ${jarfilename}"
        bat "aws lambda publish-version --function-name ${functionName}"
    }
}
