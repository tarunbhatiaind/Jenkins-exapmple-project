pipeline {
    agent any

    stages {
        stage ('build') {

            steps {
                echo 'Building the application'
            }
        }

        stage ('Test') {
			when {
				expression {
				env.BRANCH_NAME == "master" || env.BRANCH_NAME == "Test"
				}
			}
            steps {
                echo 'Test phase'
            }
        }


        stage ('Deployment Stage') {
            steps {
                echo'Deploy phase'
            }
        }
    }

} 
