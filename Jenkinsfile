pipeline {
    agent any

   stages {
       stage('k8-cluster') {
            steps {
                sh 'kubectl config use-context arn:aws:eks:ap-south-1:338658269373:cluster/prasad-eks-JuLVOQ89 '
            }
        }
         stage('deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }
         stage('service') {
            steps {
                sh 'kubectl apply -f service.yaml'
          }
        }
   }
}
