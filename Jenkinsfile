pipeline {
    agent any

   stages {
       stage('cluster') {
            steps {
               withKubeConfig(caCertificate: '', clusterName: '', contextName: '', credentialsId: 'kubecofig', namespace: '', restrictKubeConfigAccess: false, serverUrl: '') {
    // some block
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
