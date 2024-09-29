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
        
        stage('Compile Stage') {
            steps {
                sh 'mvn clean compile';
            }
        }
    }
}
