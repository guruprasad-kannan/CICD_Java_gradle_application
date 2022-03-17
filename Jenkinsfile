pipeline{
    agent any
    stages{
        stage("Sonar Quality Chek"){
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
            steps{
               script{
                   withSonarQubeEnv(credentialsId: 'mysonar') {
                       sh 'chmod +x gradlew'
                       sh './gradlew sonarqube'
                    }
               }
            }
            
        }
    }
    
}
