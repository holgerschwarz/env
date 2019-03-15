
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
    sh 'mvn -B clean verify'
}


stage 'wartem auf deployfreigabe'
node {
    timeout(time: 20, unit: 'SECONDS') {
        input 'deployen?'
    }
}


stage 'foo deploy'

node {
    echo 'start deploy'
}