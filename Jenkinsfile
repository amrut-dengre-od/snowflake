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
		sleep 100
		#mkdir -p /opt/SP/apps/
		#cp $WORKSPACE/* /opt/SP/apps/.
		whoami
		'''
            }
        }
    }
}
