pipeline {
    agent any

   stages {
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
