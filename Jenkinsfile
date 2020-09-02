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
				BRANCH_NAME == 'master' || BRANCH_NAME == 'Test'
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
