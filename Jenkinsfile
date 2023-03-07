pipeline {
    agent { 
        node {
            label 'docker-agent-python'
        }
    }
	triggers {
		pollSCM '*/5 * * * *'
	}
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd python
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
				cd python
                python3 test.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
