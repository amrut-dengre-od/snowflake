pipeline {
    agent {
        docker { image 'centos' }
    }
    stages {
        stage('Test') {
            steps {
		sh '''
                cat /etc/*release*
		hostname -i
		echo "ls before copy"; ls; pwd
		mkdir -p /opt/SP/apps/
		cp $WORKSPACE/* /opt/SP/apps/.
		ls /opt/SP/apps
		whoami
		'''
            }
        }
    }
}
