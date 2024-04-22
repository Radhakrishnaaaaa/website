pipeline {
    agent any 
    stages {
        stage ('clone') {
            steps {
                git branch:'new-feture',url:'https://github.com/Radhakrishnaaaaa/website.git'
            }
        }
        stage('git fetch'){
            steps{
                sh 'git fetch '
            }
        }
        stage('pulls'){
            steps{
                sh 'git pull origin master'
            }
        }
        stage ('build and deploy') {
            steps {
                sh ''' cp -r /var/lib/jenkins/workspace/multi-branch/* /var/www/html/app4 '''
            }
        }
    }
}
