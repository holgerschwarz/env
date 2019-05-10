
pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running "
            }
        }
    }
}

/*
pipeline {
    agent any

    stages {
        stage 'start heollworld2docker'
        node {
           sh ./de/holger/template/helloworldDocker.yml
        }



        stage 'warten auf checkout'
        node {
            timeout(time: 20, unit: 'SECONDS') {
                input 'checkout?'
            }
        }

        stage 'foo checkout'

        node {
            echo 'start checkout'
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/holgerschwarz/helloRest.git']]])
        }

        stage 'foo build'

        node {
            echo 'start build'
            sh 'mvn -B -DskipTests clean package'
        }


        stage 'foo test'

        node {
            echo 'start test'
            sh 'mvn -B verify'
        }


        stage 'warten auf deployfreigabe'
        node {
            timeout(time: 20, unit: 'SECONDS') {
                input 'deployen?'
            }
        }


        stage 'foo deploy'

        node {
            echo 'start deploy'
        }
    }
}
*/