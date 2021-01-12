pipeline {
	environment {
		HOST_DIR = ''
		CONTAINER_DIR = ''
		BIND_MOUNT_FLAG = '-v'
	}

	agent {
		docker{
			image: 'maven:3-alpine'
			args "${BIND_MOUNT_FLAG} ${HOST_DIR}:${CONTAINER_DIR}"
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
