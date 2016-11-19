#!groovy​

node {

    currentBuild.result = "SUCCESS"

    try {

        stage ('Build') {
            checkout scm
            composer install
        }

        stage ('Test') {
            echo 'Test message from jenkins file'
        }

    }
    catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }

}