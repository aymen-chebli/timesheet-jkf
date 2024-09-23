pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                git branch: 'main',
                url: 'https://github.com/aymen-chebli/timesheet-jkf.git'
            }
        }
        
        stage('clean') {
            steps {
                sh 'mvn clean';
            }
        }
        
        stage('Compile') {
            steps {
                sh 'mvn compile';
            }
        }
    }
}
