pipeline {
    agent any 

    stages {
        stage ('download and run') {
            environment  {
                ANSIBLE_HOST_KEY_CHECKING = 'False'
            }
            steps {
                sh '''
                git clone https://github.com/shegoj/systemsprovisioning.git .
                ansiblePlaybook(
                    credentialsId: 'SSH_AGENT_CONNECT', 
                    inventory: 'inventories/dev', 
                    playbook: 'playbook.yml'
                )
                '''
            }
        }
    }
}