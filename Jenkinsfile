pipeline{
    agent any
    stages1{
        stage('Build'){
            steps{
                echo 'Building the angular application'
                sh '''
                    whoami
                    ls
                    //sudo curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
                    sudo yum install nodejs -y
                    node -v; npm -v
                    sudo npm yum -g @angular/cli -y
                    git branch
                    sudo npm install
                    ls
                    ng build --prod
                    ls
                '''
            }
        }
        stage('Static Code Analysis') {
            steps{
                echo 'running static code analysis'
                sh '''
                    whoami
                    pwd
                    #ng lint --fix=true
                '''
            }
        }
        stage('Unit Test') {
            steps{
                echo 'working in the unit test stage'
            }
        }
        stage('Deploy') {
            steps{
                echo 'Deploy the content to the DEV enviroment'
                //sh '''
                //    ssh jenkins@3.17.179.193 'rm -rf /home/jenkins/angular_pipeline/dist'
                //    ssh jenkins@3.17.179.193 'mkdir -p /home/jenkins/angular_pipeline/'
                //    rsync -azvh -P /var/lib/jenkins/workspace/angular_pipeline  jenkins@3.17.179.193:/home/jenkins
                //'''
            }
        }            
    }
}