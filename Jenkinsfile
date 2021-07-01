pipeline {
  agent any
  stages {
    stage('set EKS') {
      steps {
        sh '''aws eks update-kubeconfig \\--region ap-northeast-2 \\--name jenkins-test
kubectl get svc'''
      }
    }

    stage('Create Deployment') {
      steps {
        sh '''kubectl create namespace vote
kubectl create -f k8s-specifications
'''
      }
    }

  }
}