pipeline {
    agent any   
    
    
    stages {       
        
        stage('Githut') {
            steps {
                script {
			git credentialsId: 'Git_Pass', url: "https://github.com/cssp007/ansible.git" 
                }
            }
         }
        
        stage('SSH') {
            steps {
               script {
                   sh ssh root@somnath.cssp.lab "ansible-playbook ansible.yaml"
              }
          }
      }
      

        stage('Ansible') {
            steps {
               script {
                    sh 'ansible-playbook ansible.yaml'
                }
            }
        }

}
}
