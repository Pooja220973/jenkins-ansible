pipeline {
    agent any
    stages {
        stage('Clone Git Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Pooja220973/jenkins-ansible.git'
            }
         }
        stage('Run Ansible Playbook') {
            steps {
                cd /var/lib/jenkins/workspace/jenkins-ansible
                    ansible-playbook install_apache.yml -i inventory.ini --private-key ssh_key.pem -u ansadmin

        }
    }
}
