pipeline{
    agent any
    stages{
        stage(cgeckout){
            steps{
                git branch: 'main', url: 'https://github.com/choclateboy999/ansible.git'
            }
        }
        stage(slack){
            steps{
            ansiblePlaybook credentialsId: 'a001f682-ecbd-45e2-8b3e-287f9f1f2431', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'mkdir.yml'
            }
        }
    }
}
