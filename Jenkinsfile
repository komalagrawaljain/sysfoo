pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh 'mvn compile'
        echo 'ddfhsdfksdf'
      }
    }

    stage('test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package -DskipTests'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}