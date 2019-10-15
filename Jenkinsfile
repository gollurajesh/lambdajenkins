def bucket = 'demos3terraform'
def functionName = 'TestJavaJenkins'
def region = 'us-east-1'
def jarfilename = "lambdajenkins${BUILD_NUMBER}"
def projectname = "demo-1.0.0.jar"

node{
    stage('Checkout'){
        checkout scm
    }
    stage('Build'){
        bat "mvn clean install
    }
    stage('Push'){
        build job: 'terraformtest'   	
    }
}
