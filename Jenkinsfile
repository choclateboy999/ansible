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
                sh 'ansible-playbook mkdir.yml -i hosts'
            }
        }
    }
}
