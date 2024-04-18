pipeline {
    agent any
    stages {
        stage('Compile') {
            steps {
                sh './gradlew compileJava'
            }
        }
        stage('Unit test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Code coverage') {
            steps {
                step{
                   sh './gradlew test jacocoTestReport' 
                }
                step{
                    sh './gradlew test jacocoTestCoverageVerification'
                } 
            }
        }
    }
}
