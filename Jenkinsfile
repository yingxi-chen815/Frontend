pipeline {
    agent any
    stages {
	stage('begin'){
		steps {
                sh '''#!/bin/bash
                        # jenkins下的目录
                        JENKINS_HOME= "/var/jenkins_home/workspace/frontend_test"
                        
                        # 等待三秒
                        echo sleep 3s
                        sleep 1
                        echo sleep 2s
                        sleep 1
                        echo sleep 1s
                        sleep 1
                              
                        echo "结束进程完成"
			
                        # SERVER_NAME=backend_test
			
                        # JENKINS_HOME
                        cd /var/jenkins_home/workspace/frontend_test
                        
                        # JENKINS_HOME
                        cp -r /var/jenkins_home/workspace/frontend_test/docker/Dockerfile /var/jenkins_home/workspace/frontend_test/target
			                  echo "update cp"
                        
                        # 修改文件权限  JAR_NAME
                        # chmod 755 School-0.0.1-SNAPSHOT.jar
                        
                        docker -v
                        
                        docker stop dfs-frontend-img
                        docker rm dfs-frontend-img
                        docker rmi dfs-frontend-img
                        
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
