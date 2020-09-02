pipeline {
    agent any
	
	environment {
		NEW_VERSION = '1.3.0'
	}
	
	parameters {
		
		choice(name : 'VERSION', choices :['1.1.0','1.2.0','1.3.0'], description : '')
		booleanParam(name: 'executeTests', defaultValue: true, description: '' )	
	}
    stages {
        stage ('build') {

            steps {
                echo 'Building the application'
				echo "Building version ${NEW_VERSION}"
            }
        }

        stage ('Test') {
			when {
				expression {
				
				//env.BRANCH_NAME == "master" || env.BRANCH_NAME == "Test"
				params.executeTests
				}
			}
            steps {
                echo 'Test phase'
            }
        }


        stage ('Deployment Stage') {
            steps {
                echo'Deploy phase'
				echo "deploying version ${params.VERSION}"
            }
        }
    }

} 
