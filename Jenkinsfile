/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.8.6-openjdk-11-slim' } }
    stages {
        stage('build') {
            steps {
	        sh 'echo "Build-Stage"'
                sh './gradlew --version'
		sh './gradlew build'
            }
        }
	stage('test') {
	    steps {
	    sh 'echo "Test-Stage"'
	    sh './gradlew test'
	    }
	}
    }
}
