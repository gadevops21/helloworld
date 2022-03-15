pipeline {
  agent any
  tools {
      maven 'M2_HOME'
  }
  environment {
    registry = "gacobby/devop-pipeline"
    registryCredential = 'dockerhub'
  }
  stages {
    stage('Build'){
      steps {
        sh 'mvn clean'
        sh 'mvn install'
        sh 'mvn package'   
      }
    }
     stage('test'){
      steps {
        echo "test step"
        sh 'mvn test'
      }
    }
     stage('deploy'){
      steps {
        echo "deploy step"
        sleep 10
      }
    }
  }
}
