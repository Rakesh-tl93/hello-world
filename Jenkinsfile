pipeline {
    agent {label'newnode'}

    stages {
        stage('BUILD') 
        {
            steps {
                git branch:'main',url:
                'https://github.com/Rakesh-tl93/hello-world'
                sh '''cd /home/ec2-user/jenkins/workspace/newpipeline 
                mvn clean install'''
            }
        }
        stage('DEPLOY') 
        {
            steps {
            sh '''cd /home/ec2-user/jenkins/workspace/newpipeline/target 
            sudo cp *.war /opt/apache-tomcat-10.0.27/webapps'''
            }
        }
    }
}
