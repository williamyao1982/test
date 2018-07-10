pipeline {
  agent any
  stages {
    stage('test1') {
      steps {
        sh 'echo "hello world!"'
      }
    }
    stage('k8s') {
      steps {
        withKubeConfig(serverUrl: 'http://16.178.115.5:8080') {
          sh 'kubectl get pod'
        }

      }
    }
  }
}