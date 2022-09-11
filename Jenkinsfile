pipeline{
    agent any
    stages{
        stage("cgeckout"){
            steps{
                git branch: 'main', url: 'https://github.com/choclateboy999/ansible.git'
            }
        }
        stage("build"){
                         steps{
                                sh 'mvn compile package'
               }
           }
        stage("ansible"){
            steps{
                  ansiblePlaybook credentialsId: 'tomcat', disableHostKeyChecking: true, installation: 'ansible', inventory: 'prod', playbook: 'mkdir.yml'
            }
        }
    }
}
