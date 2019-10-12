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
            withMaven(maven : 'apache-maven-3.6.2') {
                bat'mvn clean compile'
            }
           
        }
    }
}