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
                mtaBuild script: this
            }
        }

        stage('attach') {
            steps {
                transportRequestUploadFile script: this,
                transportRequestId: 'S4DK900047' 
            }
        }
    }
}