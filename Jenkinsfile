pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis/shelll') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=simple-java-maven-app \\
  -Dsonar.projectName=\'simple java maven app\' \\
  -Dsonar.host.url=http://10.10.1.155:9000 \\
  -Dsonar.token=sqp_860138ea8e8a671a05711a67c18c2963f59686b1'''
      }
    }

    stage('Unit Test /') {
      steps {
        sh './mvnw "-Dtest=**/petclinic/*/*.java" test'
      }
    }

    stage('package/') {
      steps {
        sh './mvnw package -DskipTests=true'
      }
    }

  }
}