pipeline {
        agent any

        tools{
                maven 'Maven'
        }
        stages {
         
          stage("build & SonarQube Scanner") {
            steps {
              withSonarQubeEnv('sonarqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
