pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat "mvn -Dmaven.test.failure.ignore=true clean install -U -e -DskipTests"
      }
    }

  }
}
