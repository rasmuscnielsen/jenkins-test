#!groovy​

node {

    currentBuild.result = "SUCCESS"

    try {

        stage ('Build') {
            checkout scm
            sh 'composer install'
        }

        stage ('Test') {
            sh 'phpunit'
        }

    }
    catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }

}