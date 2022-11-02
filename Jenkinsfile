pipeline {
  environment {
    repo = "binu119/dockerpipeline"
  }
  agent any
  stages {
    stage('Install Docker') {
      steps {
        sh 'ansible-playbook Ansible/dockerinstall.yaml'
      }
    }
    stage('Deploy container') {
      steps {
        sh 'ansible-playbook Ansible/deploycontainer.yaml -e "image_name=$repo image_tag=latest"'
      }
    } 
  }
}
