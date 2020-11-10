pipeline {
  agent any
  tools{
    maven 'Maven'
    jdk 'JDK 8'
  }
  stages {
    stage('Build') {
      steps {
        bat "mvn -Dmaven.test.failure.ignore=true clean install -U -e -DskipTests"
      }
    }

  }
}
