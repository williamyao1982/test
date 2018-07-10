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
        withKubeConfig(serverUrl: 'https://16.178.115.5:6443', credentialsId: 'admin', caCertificate: '/etc/kubernetes/ssl/ca.pem') {
          sh 'kubectl get pod'
        }

      }
    }
  }
}