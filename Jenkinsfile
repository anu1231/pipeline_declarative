pipeline {

	agent any 
	environment {
		NEW_VERSION='1.3.0'
	}
	parameters {
		
            choice(
            choices: ['greeting' , 'silence'],
            description: '',
            name: 'REQUESTED_ACTION')
	}
	stages {
      		stage("build") {
			steps {
				echo "BUILD NUMBER IS ${BUILD_NUMBER}"
				echo "building stage"
                
             			 }

			}
		stage("test") {
   				when {
					expression {
							params.REQUESTED_ACTION=='greeting'
						}
					}
			        steps {
					echo "testing stage"
     					 }
				}
		stage("deploy") {
  				 steps {
					 echo "${NEW_VERSION}"
					echo "deploying stage"
					}

				}
			}
	
}

