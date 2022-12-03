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
    
                '''
                echo '运行成功'
            }
	}
    }
}
