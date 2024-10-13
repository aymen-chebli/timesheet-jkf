pipeline {
    agent any
    tools {
		jdk 'JAVA_HOME',
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                git branch: 'main',
                url: 'https://github.com/aymen-chebli/timesheet-jkf.git'
            }
        }
        
        stage('CLEAN AND COMPILE STAGE') {
            steps {
                sh 'mvn clean compile';
            }
        }
		
		stage('MVN SONARQUBE') {
            steps {
                sh 'mvn sonar:sonar';
            }
        }
    }
}
