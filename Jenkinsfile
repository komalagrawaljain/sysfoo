pipeline {
  agent none
  stages {
    stage('compile') {
      agent {
        docker {
          image 'maven:3.9.6-eclipse-temurin-17'
        }

      }
      steps {
        sh 'mvn compile'
        echo 'ddfhsdfksdf'
      }
    }

    stage('test') {
      agent {
        docker {
          image 'maven:3.9.6-eclipse-temurin-17'
        }
      }
      steps {
        sh 'mvn clean test'
      }
    }

    stage('package') {
      agent {
        docker {
          image 'maven:3.9.6-eclipse-temurin-17'
        }
      }
      steps {
        sh 'mvn package -DskipTests'
      }
    }
  }
}
