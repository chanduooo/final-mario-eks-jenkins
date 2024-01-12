pipeline {
    agent any

   stages {
       stage('cluster') {
            steps {
                withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'education-eks-3dNbsID2', contextName: ' arn:aws:eks:ap-south-1:338658269373:cluster/education-eks-3dNbsID2', credentialsId: 'kubecofig', namespace: '', serverUrl: 'https://89DEE8A651C9B3A546B296FED053258F.gr7.ap-south-1.eks.amazonaws.com']]) {
    
                }
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
