pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean install -U -e -DskipTests'
      }
    }

    stage('Test') {
      steps {
        bat ' mvn -Dmaven.repo.local=C:/Users/sushmitha/.m2/repository test'
      }
    }

    stage('Deploy') {
      steps {
        bat 'mvn package deploy -DmuleDeploy -Danypoint.username=njctrail -Danypoint.password=Njc@1234 -DapplicationName=jenkins-demo-sls '
      }
    }

  }
  tools {
    maven 'Maven'
    jdk 'JDK 8'
  }
}
