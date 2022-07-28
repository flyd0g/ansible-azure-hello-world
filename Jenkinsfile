pipeline {
  agent any
  
  environment {
   ANSIBLE_PRIVATE_KEY=credentials('azure_vm_private_key') 
  }
  
  stages {
    stage('Build') {
      steps {
        sh 'ansible-playbook -i hosts -u adam --private-key=$ANSIBLE_PRIVATE_KEY site.yml'
      }
    }
  }
}
