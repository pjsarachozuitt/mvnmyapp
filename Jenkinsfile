pipeline {
	agent any
	stages {
		stage('clean') {
			steps {
				sh "mvn clean"
			}
		}
		stage('test') {
			steps {
				sh "mvn test"
			}
		}
		stage('build') {
			steps {
				sh "mvn package"
			}
		}
	}
	tools {
        maven 'Maven 3.6.2'
    }
}