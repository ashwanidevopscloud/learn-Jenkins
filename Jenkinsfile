pipeline {
    agent {
        label 'AGENT-2'
    }
    options{
        timeout(time:10, unit:'SECONDS')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is build'
                // sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is deploy'
            }
        }

    }
    post{
        always{
            echo "This section runs always"
            deleteDir()
        }
    }
}
