node {

    stage('Clone repository') {
        checkout scm
    }
	
	
    stage('Build image') {
        /* This builds an image with all pytest selenium scripts in it */
        docker.build("pytest-with-src")
    }
}
