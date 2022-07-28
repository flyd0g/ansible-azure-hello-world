pipeline {
  agent any
  
//  environment {
//   ANSIBLE_PRIVATE_KEY=credentials('azure-key') 
//  }
  
  stages {
    stage('Build') {
      steps {
        sh 'ansible-playbook -i hosts site.yml'
      }
    }
  }
}
