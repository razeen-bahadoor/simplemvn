pipeline {


     def HOST_DIR = '/root/.m2'
     def CONTAINER_DIR = '/root/.m2'

    agent {
        docker {
            image 'node:14-alpine'
            args "-v ${HOST_DIR}:${CONTAINER_DIR}"
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
