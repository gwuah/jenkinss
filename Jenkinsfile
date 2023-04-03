#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
                script {
                    String[] projects;
                    changeset = sh (script: './changed_services', returnStdout: true).trim().split(" ").sort(false).join(" ")

                    onlyMitra = "//mitra/cmd/mitra:base"
                    onlyHydra = "//hydra/cmd/hydra:base"
                    onlyHydraAndMitra = "//hydra/cmd/hydra:base //mitra/cmd/mitra:base"

                    if onlyHydra || onlyMitra || onlyHydraAndMitra {
                        println("integrations team")
                    } else {
                        println("other team")
                    }
                    
                }
            }
        }
    }
}
