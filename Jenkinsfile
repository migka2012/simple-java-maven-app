pipeline {
    agent any

    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }

        stage("Delivery") {
            steps {
              sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
            }
        }
    }
}
