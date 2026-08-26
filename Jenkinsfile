pipeline {
    agent any
    environment {
		x = 200
		y = 300
	}
    stages {
	
        stage('Build Information'){
         steps{
               echo 'Yello printing'
			   sh 'echo $BUILD_ID'
			   sh 'echo $JOB_NAME'
            }
        }
        stage('Show linux command output'){
             steps{
               echo 'Green printing'
               sh 'date'
               sh 'whoami'
               sh 'id'
            }
        }
        stage('Show custom variable value'){
              steps{
               echo 'Red printing'
			   sh 'echo $x'
			   sh 'echo $y'
            }
        }
    }
}
