pipeline {
    agent {
        Dockerfile true
    }

    stages {
	    stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'feaaf2b8-524d-4ead-bdba-65d12938a0ff', url: 'https://github.com/akanksha2897/apache_new.git']]])
            }
        }
        stage('Build') {
            steps {
                echo 'Job is being build'
                bat label: '', script: 'docker build'
            }
        }
        stage('Test') {
            steps {
                echo 'Job is being Test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Job is being Deploy'
            }
        }
    }
}
