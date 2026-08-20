pipeline{
    agent any
    stages {
        stage( 'shell commands') {
            steps {
                echo 'user:'
                sh 'whoami'

                echo 'directory:'
                sh 'pwd'

                echo 'list files:'
                sh 'ls -a'
            }
        }
        stage( 'version commands') {
            steps {
                echo 'java version:'
                sh 'java -version'

                echo 'docker installation:'
                sh 'sudo apt install docker.io -y'

                echo 'docker version:'
                sh 'docker -version'

                echo 'jenkins version:'
                sh 'jenkins -version'
            }
        }
    }
    post {
        always {
            echo 'commands executed'
        }
        success {
            echo 'commands executed successfully'
        }
        failure {
            echo 'commands failed to execute'
        }
       cleanup {
            echo 'cleaning up'
        }
    }
}
