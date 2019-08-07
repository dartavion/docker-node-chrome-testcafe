pipeline {
    agent any
    docker {
        image 'node: 8'
        image 'timbru31/node-chrome'
    }
    
    stage ('Pre') {
        steps {
            checkout scm
            sh 'testcafe chrome:headless ./tests'
        }
    }
}