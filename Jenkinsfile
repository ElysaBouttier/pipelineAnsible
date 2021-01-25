properties([pipelineTriggers([githubPush()])])

pipeline {
    agent { 
      dockerfile true
    }
    
    options {
	withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'ynov_24', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']])
    }
	
    environment {
	AWS_REGION = 'eu-west-3'
    }
}
