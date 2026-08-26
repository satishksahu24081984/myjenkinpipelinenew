
pipeline {
    agent any
    environment {
		x = 400
		y = 800
		git_token = 'github-token'
		docker_token = 'docker-token'
	}
	parameters {
        string(name: 'person', defaultValue: 'Ekamjeet Singh', description: 'Enter your username to continue this Job')
		
    }
	triggers {
        githubPush()   // reacts to GitHub webhook events
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
			   sh 'echo  $git_token'
			  sh 'echo  $docker_token'
            }
        }
		stage('Show Parameters values'){
              steps{
				sh  'echo $person'
			
            }
        }
    }
}
