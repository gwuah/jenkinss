#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
                script {
                    CHANGED = sh (script: './y', returnStdout: true).trim()
                    String[] projects;
                    projects = CHANGED.split(" ").sort(false)
                    
                    println(projects.size())

                    println projects[0]
                }
            }
        }
    }
}
