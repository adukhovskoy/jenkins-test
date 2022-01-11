pipeline {
  agent { label '!master' }
  stages {
    stage('Checkout repo'){
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[port:'443', url: 'https://github.com/adukhovskoy/jenkins-test.git']]])
      }
    }
    stage('Test'){
      steps {
        sh '''
        ls -alh
        '''
      }
    }
  }
}
