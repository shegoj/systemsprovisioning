pipeline {
    agent any 

    stages {
        stage ('download and run') {
            steps {
                sh '''
                git clone https://github.com/shegoj/systemsprovisioning.git .
                 #ansible-playbook -i inventories/dev playbook.yml
                '''
            }
        }
    }
}