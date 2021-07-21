pipeline{
	agent any
	stages {
		stage('BUILD') {
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: BUILD
				'''
			}	
		}
		
		stage('TEST') {
			parallel { 
				stage('TEST1') {
					steps {
						sh 'sleep 5'	
						echo "TESTING PHASE1"
					}	
					
				}
				stage('TEST2') {
					steps {
						sh 'sleep 5'	
						echo "TESTING PHASE2"
					}	
					
				}
				stage('TEST3') {
					steps {
						sh 'sleep 5'	
						echo "TESTING PHASE3"
					}	

				}
		

		stage('DEPLOY') {
			agent any
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: DEPLOY
				'''
					}	
				}
			}
		}
	}
}
