pipeline { 
    agent any  

    stages { 
    	stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
        stage('Build') { 
            steps {
	            withMaven(maven : 'apache-maven-3.6.1') {
	                bat'mvn clean compile'
	            }
	        }
        }
    }
}