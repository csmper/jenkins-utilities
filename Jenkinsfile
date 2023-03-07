pipeline {
    agent { 
        node {
            label 'docker-agent-python'
        }
    }
	triggers {
		pollSCM '* * * * *'
	}
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd myapp
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
				cd myapp
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
