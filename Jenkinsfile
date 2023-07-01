pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\

























-Dsonar.projectKey=simple-java-maven-app \\     


                 

































-Dsonar.projectName=\'simple java maven app\' \\    -Dsonar.host.url=http://10.10.1.155:9000 \\ -Dsonar.token=sqp_860138ea8e8a671a05711a67c18c2963f59686b1'''
      }
    }

  }
}