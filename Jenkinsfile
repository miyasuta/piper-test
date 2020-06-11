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
                echo "stage: attach"
            }
        }
    }
}