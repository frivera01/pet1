#!groovy

pipeline {
  agent none
  stages {
  /*  stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    } */
    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t muchast2/spring-petclinic:latest .'
      }
    }
    stage('Docker run')
      agent any
      steps {
        sh 'docker run -p 8081:8080 muchast2/spring-petclinic:'
    }
  }
}