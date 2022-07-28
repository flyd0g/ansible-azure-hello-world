pipeline {
  agent any
  
  environment {
   ANSIBLE_PRIVATE_KEY=credentials('azure-key') 
  }
  
  stages {
    stage('Build') {
      steps {
        sh 'ansible-playbook -i hosts --private-key=$ANSIBLE_PRIVATE_KEY site.yml'
      }
    }
  }
}
