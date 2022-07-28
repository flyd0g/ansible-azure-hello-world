pipeline {
  agent any
  
  environment {
   ANSIBLE_PRIVATE_KEY=credentials('azure_vm_private_key') 
  }
  
  stages {
    stage('Build') {
      steps {
        ansiblePlaybook become: true, installation: 'ansible-adam', inventory: 'hosts', playbook: 'site.yml', vaultCredentialsId: 'azure_vm_private_key'
      }
    }
  }
}
