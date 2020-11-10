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
        bat ' mvn -f pom.xml -Denv=dev -Dkey=mule test'
      }
    }

    stage('Deploy') {
      steps {
        bat 'mvn -f pom.xml package deploy -DmuleDeploy -Danypoint.username=njctrail -Danypoint.password=Njc@1234 -DapplicationName=jenkins-demo '
      }
    }

  }
  tools {
    maven 'Maven'
    jdk 'JDK 8'
  }
}
