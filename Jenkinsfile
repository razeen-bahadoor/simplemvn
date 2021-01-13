pipeline {
	environment {
		HOST_DIR = '~/.m2'
		CONTAINER_DIR = '~/.m2'
	}

    agent {
        docker {
            image 'node:14-alpine'
            args "-v ~/.m2:~/.m2"
         }
     }


	stages {

		stage("build") {

			steps {
				sh 'mvn -B -DskipTests clean package' 
			}
		}
		
	}
}
