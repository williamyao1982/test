pipeline {
  agent any
  stages {
    stage('test1') {
      steps {
        sh '''kubectl get pod
kubectl get svc'''
      }
    }
  }
}