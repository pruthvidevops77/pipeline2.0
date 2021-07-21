pipeline {
	agent any
	parameters {
		choice(name: 'TARGET_ENV', choices: ['test', 'prod'], description: 'target environment to deploy')
	}
	environment {
		DEPLOY_TO = "${TARGET_ENV}"
	}
	stages {
		stage('DEPLOY_TEST') {
		      when {
			      environment name: 'DEPLOY_TO', value: 'test'
		      }
		      steps {
			      echo 'DEPLOY_TO TEST ENVIRONMENT ....'
			      sh 'sleep 5'
		      }
		}
		stage('DEPLOY_PROD') {
		      when {
			      environment name: 'DEPLOY_TO', value: 'prod'
		      }
		      steps {
			      echo 'DEPLOY_TO PRODUCTION ....'
			      sh 'sleep 5'
		      }
		}
	}
}
