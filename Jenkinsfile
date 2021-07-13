pipeline			//In declarative pipeline you have to put all in stages
	{	
	agent { docker { image 'maven:3.8.1'} }       //this is how you use docker in agents. Can be java or nodejs 
	stages {
		stage('Build') {
			steps {
	echo "build"
	}}
	stages {
		stage('Test') {
			steps {
	echo "Test"
	}}
	}}
	post {
	always {
		echo "i'm awesome"
		}}}
