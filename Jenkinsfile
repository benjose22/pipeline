node {

    stage('Clone repository') {
        checkout scm
    }
	stage("Stage with input") {
    steps {
      def userInput = false
        script {
            def userInput = input(id: 'Proceed1', message: 'Promote build?', parameters: [[$class: 'BooleanParameterDefinition', defaultValue: true, description: '', name: 'Please confirm you agree with this']])
            echo 'userInput: ' + userInput

            if(userInput == true) {
                // do action
            } else {
                // not do action
                echo "Action was aborted."
            }

        }    
    }  
	}
	
    stage('Build image') {
        /* This builds an image with all pytest selenium scripts in it */
        docker.build("pytest-with-src")
    }
}
