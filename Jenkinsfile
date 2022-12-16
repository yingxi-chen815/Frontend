pipeline {
    agent any
    stages {
	  stage('begin'){
		steps {
            sh '''#!/bin/bash
                    # jenkins
                    JENKINS_HOME= "/var/jenkins_home/workspace/frontend_test"
                            
                    # SERVER_NAME=backend_test
        
                    # JENKINS_HOME
                    cd /var/jenkins_home/workspace/frontend_test
                    
                    # JENKINS_HOME
                    cp -r /var/jenkins_home/workspace/frontend_test/docker/Dockerfile /var/jenkins_home/workspace/frontend_test/target
                    echo "update cp"
            '''
            }
	    }
        stage('run docker') {
            steps {
                sh '''
                        docker -v
                        pwd
                        
                        # stop existing container
                        #docker stop dfs-frontend-img
                        #docker rm dfs-frontend-img
                        #docker rmi dfs-frontend-img
                        
                        echo "start build"
                        docker build -t dfs-frontend-img -f docker/Dockerfile .
                        docker run -d -p 8002:80 --name dfs-frontend-img dfs-frontend-img
                        echo "finished"

                '''
                echo 'completed'
            }
        }
    }
}
