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
                sh 'mvn sonar:sonar \
                -Dsonar.projectKey=achat \
                -Dsonar.host.url=http:172.10.0.140:9000 \
                -Dsonar.login=00667aa3f3315e767951ba1f09c22a9c992038c6';
                echo 'Maven sonarqube...';
            }
        }
    }
}
