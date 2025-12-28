pipeline {
	agent any

	stages {
		stage('Build JAR') {
			steps {
				sh 'mvn clean package -DskipTests'
			}
		}

		stage('Build Docker Image') {
			steps {
				sh 'docker build -t demo-ci-cd .'
			}
		}
	}
}
