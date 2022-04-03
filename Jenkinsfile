pipeline {
    agent any 

    stages {
        stage ('download and run') {
            environment  {
                ANSIBLE_HOST_KEY_CHECKING = 'False'
            }
            steps {
               echo  'simple stuff'
            }
        }
    }
    post {
        always {
            deleteDir()
        }
    }
}