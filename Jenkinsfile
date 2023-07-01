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
        sh ''' mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=simple-java-maven-app \\
  -Dsonar.projectName=\'simple java maven app\' \\
  -Dsonar.host.url=http://43.204.195.107:9000 \\
  






'''
      }
    }

  }
}