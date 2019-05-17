
pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running "
            }
        }

        stage('copy') {
            steps {

                sh 'sudo docker ps -a '
            }
        }

        stage ('foo checkout') {
            steps {
                echo 'start checkout'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/holgerschwarz/helloRest.git']]])
            }
        }
    }
}
