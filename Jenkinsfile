pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' //download later as needed
            }
        }
	  stage('Unit Tests') {
            steps {
              sh "mvn test"
			}
		}
    }
}