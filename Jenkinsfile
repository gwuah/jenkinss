#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
                script {
                    CHANGED = sh (script: './y', returnStdout: true).trim()
                }

                // sh "echo "hello""
                sh 'echo $(pwd)'
                // sh 'echo $(ls -l)'
                println CHANGED

                @split = CHANGED.split(" ")

                println @split[0]

            }
        }
    }
}
