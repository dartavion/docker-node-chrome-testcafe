#!/usr/bin/env groovy
pipeline {
    agent {
      docker {
          image 'node: 8'
          image 'timbru31/node-chrome'
      }
    }
    stages {
      stage ('Pre') {
          steps {
              checkout scm
              sh 'testcafe chrome:headless ./tests'
          }
       }
    }
}