pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /home/ws355/.m2:/root/.m2'
        }
    }
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
