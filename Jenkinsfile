node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integraiton Test') {
		echo "Test"
	}
	stage('Package') {
		steps {
			sh "mvn package -DskipTests"
		}
	}
	stage('Build Docker image') {
		steps {
	//primitive or declarative method "docker build -t in28min/currency-exchange-devops:$env.BUILD_TAG"	
			script {
				dockerImage = docker.build("sunilbalu/hello-world-python:${env.BUILD_TAG}")	
	}
	}
	stage('Push Docker image') {
		steps {
			script {
				docker.withRegistry('', 'sunilbalu') {
	dockerImage.push();
				dockerImage.push('Latest');
	}
		}
	}	
}
