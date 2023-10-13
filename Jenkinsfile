pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q Portfolio-website"
                bat "git clone https://github.com/raghvendra0898/Portfolio-website.git"
                bat "mvn clean -f Portfolio-website"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Portfolio-website"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Portfolio-website"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Portfolio-website"
            }
        }
    }
}
