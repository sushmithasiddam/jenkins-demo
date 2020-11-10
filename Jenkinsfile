pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'bat "mvn -Dmaven.test.failure.ignore=true clean install -U -e -DskipTests"'
      }
    }

  }
}