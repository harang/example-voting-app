pipeline {
  agent any
  stages {
    stage('set EKS') {
      steps {
        sh '''aws configure
\\ AKIA4J275QUWCAX22O2R
\\ M9PAjJ5gbXYsJbbE7DtvWaOQVQxdGCzobQjnzLDm
\\ ap-northeast-2
\\ json'''
        sh '''aws eks update-kubeconfig \\--region ap-northeast-2 \\--name jenkins-test
'''
        sh 'kubectl get svc'
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