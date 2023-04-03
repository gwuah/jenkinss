#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
                script {
                    changeset = sh (script: './only_hydra', returnStdout: true).trim().split(" ").sort(false).join(" ")

                    onlyMitra = '//mitra/cmd/mitra:base' == changeset
                    onlyHydra = '//hydra/cmd/hydra:base' == changeset
                    onlyHydraAndMitra = '//hydra/cmd/hydra:base //mitra/cmd/mitra:base' == changeset

                    if (onlyHydra || onlyMitra || onlyHydraAndMitra) {
                        println("integrations team")
                    } else {
                        println("other team")
                    }


                    changeset = sh (script: './only_mitra', returnStdout: true).trim().split(" ").sort(false).join(" ")

                    onlyMitra = '//mitra/cmd/mitra:base' == changeset
                    onlyHydra = '//hydra/cmd/hydra:base' == changeset
                    onlyHydraAndMitra = '//hydra/cmd/hydra:base //mitra/cmd/mitra:base' == changeset

                    if (onlyHydra || onlyMitra || onlyHydraAndMitra) {
                        println("integrations team")
                    } else {
                        println("other team")
                    }

                    changeset = sh (script: './only_hydra_mitra', returnStdout: true).trim().split(" ").sort(false).join(" ")
                    onlyMitra = '//mitra/cmd/mitra:base' == changeset
                    onlyHydra = '//hydra/cmd/hydra:base' == changeset
                    onlyHydraAndMitra = '//hydra/cmd/hydra:base //mitra/cmd/mitra:base' == changeset

                    if (onlyHydra || onlyMitra || onlyHydraAndMitra) {
                        println("integrations team")
                    } else {
                        println("other team")
                    }

                    changeset = sh (script: './other', returnStdout: true).trim().split(" ").sort(false).join(" ")
                    onlyMitra = '//mitra/cmd/mitra:base' == changeset
                    onlyHydra = '//hydra/cmd/hydra:base' == changeset
                    onlyHydraAndMitra = '//hydra/cmd/hydra:base //mitra/cmd/mitra:base' == changeset

                    if (onlyHydra || onlyMitra || onlyHydraAndMitra) {
                        println("integrations team")
                    } else {
                        println("other team")
                    }
                    
                }
            }
        }
    }
}
