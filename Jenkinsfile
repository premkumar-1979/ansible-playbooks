node {
   
    
    stage('gitclone') {
       git credentialsId: '125e426e-8bec-43ab-9282-96a7f24dcea4', url: 'https://github.com/premkumar-1979/ansible-playbooks.git'
       sh label: '', script: '''cd /var/tmp
                                git clone https://github.com/premkumar-1979/ansible-code.git/
                                cd ansible-code
                                ls -al'''
    }
    
    stage ('ansible command') {
        sh ''' cd /var/tmp/ansible-code
                ansible-playbook --syntax-check firstplaybook.yml'''
    }
    
    stage ('removingdirectory') {
        
        sh 'rm -rf /var/tmp/ansible-code'
    }
    
}
