pipeline {
	agent any
	tools {
        maven 'maven3.6.2'
    }
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
	post {
		success {
			sh "git push heroku master"
		}
	}
}