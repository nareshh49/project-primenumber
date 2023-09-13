pipeline {
    agent any
    tools {
        maven "Maven 3.8.6"
    }
    stages {
        stage('Build Artifact') {
            steps {
               sh "mvn clean package -DskipTests=tre"
               archive 'target/*..jar' 

        stage('Test MAven - Junit') {
            steps {
                sh "mvn test'"
            }
            post{
               always{
                junit 'target/surefire-reports/*.xml'
               }
            }
        } 

               }


            }
        }
}

