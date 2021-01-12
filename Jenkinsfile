pipeline {
	environment {
		HOST_DIR = '/root/.m2'
		CONTAINER_DIR = '/root/.m2'
	}

    agent {
        docker {
            image 'node:14-alpine'
            args "-v ${env.HOST_DIR}:${env.CONTAINER_DIR}"
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
