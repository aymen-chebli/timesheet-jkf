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
        
        stage('CLEAN AND COMPILE STAGE') {
            steps {
                sh 'mvn clean compile -DskipTests';
            }
        }
        
        /* 
        stage('MVN SONARQUBE') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.login=sqa_69398ed610b6c6ed9df81e50d9c82630c276520d'
            }
        }
        */
        
        stage('MVN BUILD') {
            steps {
                sh 'mvn install -DskipTests'
            }
        }
        
        stage('MVN DEPLOY') {
            steps {
                sh 'mvn deploy -DskipTests'
            }
        }
    }
}
