pipeline{
agent any
stages{
stage('checkout'){
steps{
   git branch: 'main', credentialsId: 'git_user', url: 'https://github.com/sheershikasaineni/jenkins-ansible.git'
   }
}
stage('ansibleexecution'){
steps{ 
   ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''
     }
}
}
}
