node {
   
    
    stage('gitclone') {
        
       sh '''cd /var/tmp
        git clone https://github.com/premkumar-1979/ansible-code.git/
        cd ansible-code
        ls -al '''
    }
    
    stage ('ansible command') {
        sh ''' cd /var/tmp/ansible-code
                ansible-playbook --syntax-check firstplaybook.yml'''
    }
    
    stage ('removingdirectory') {
        
        sh 'rm -rf /var/tmp/ansible-code'
    }
    
}
