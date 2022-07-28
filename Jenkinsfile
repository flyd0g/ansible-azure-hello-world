pipeline {
  agent any
  
  environment {
   ANSIBLE_PRIVATE_KEY=credentials('5feabb1a-e90e-4a2f-adec-999dddacd02d') 
  }
  
  stages {
    stage('Build') {
      steps {
        sh 'ansible-playbook -i hosts --private-key=$ANSIBLE_PRIVATE_KEY site.yml'
      }
    }
  }
}
