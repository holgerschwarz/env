
pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running "
            }
        }

        stage ('foo checkout') {
            node {
                echo 'start checkout'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/holgerschwarz/helloRest.git']]])
            }
        }
    }
}
