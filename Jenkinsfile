pipeline {

	agent any 
	enviroment {
		NEW_VERSION='1.3.0'
	}
	parameters {
		string(name:first,defaultvalue:'',description:'')
	}

	stages {
      		stage("build") {
			steps {
				echo "BUILD NUMBER IS ${BUILD_NUMBER}"
				echo "building stage"
                
             			 }

			}
		stage("test") {
   				steps {
					when {
						expression{
							params.first
						}
					}
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

