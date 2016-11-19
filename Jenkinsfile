#!groovy​

node {

    currentBuild.result = "SUCCESS"

    try {

        stage 'Checkout'
            checkout scm

        stage 'Test'
            echo 'Test message from jenkins file'

    }
    catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }

}