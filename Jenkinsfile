@Library('piper-lib-os') _


pipeline {

    agent any

    stages {
        stage("prepare") {
            steps {
                deleteDir()
                checkout scm
                setupCommonPipelineEnvironment script: this
            }
        }

        stage('build') {
            steps {
                echo "build"
            }
        }

        stage('attach') {
            steps {
                echo "attach"
            }
        }
    }
}