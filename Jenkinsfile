pipeline {
    agent any
    stages {
        stage('Checkout GIT'){
            steps {
                echo 'Pulling...';
                git branch: 'main',
                url : 'https://github.com/WaelBouatay/Achat-DevOps';
            }
        }
        stage('MVN CLEAN'){
            steps {
                sh 'mvn clean';
                echo 'Maven clean...';
            }
        }
        stage('MVN COMPILE'){
            steps {
                sh 'mvn compile';
                echo 'Maven compile...';
            }
        }
         stage('MVN SONARQUBE'){
            steps {
                sh 'mvn sonarqube';
                echo 'Maven sonarqube...';
            }
        }
    }
}
