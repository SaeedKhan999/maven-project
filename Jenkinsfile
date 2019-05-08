pipeline {
    agent any

    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
                    }
        }
        stage('run'){
            steps{
                sh "docker run -d -p 8081:8080 tomcatwebapp:${env.BUILD_ID}"

               }
            }
          }
       }
