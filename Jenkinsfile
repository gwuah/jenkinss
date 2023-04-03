#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
                script {
                    CHANGED = sh (script: './y', returnStdout: true).trim()
                
                    // sh "echo "hello""
                    // sh 'echo $(ls -l)'
                    // sh 'echo $(pwd)'

                    println CHANGED

                    String[] projects;
                    projects = CHANGED.split(" ")

                    println projects[0]
                }
            }
        }
    }
}
