pipeline{
    agent any
    stages{
        stage("cgeckout"){
            steps{
                git branch: 'main', url: 'https://github.com/choclateboy999/ansible.git'
            }
        }
        stage("ansible"){
            steps{
                   ansiblePlaybook credentialsId: 'tomcat', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'mkdir.yml'
            }
        }
    }
}
