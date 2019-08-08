#!/usr/bin/env groovy
pipeline {
    agent {
      docker {
          image 'timbru31/node-chrome'
          image 'testcafe/testcafe'
      }
    }
    stages {
      stage ('Pre') {
          steps {
              checkout scm
              sh 'npm -v'
              sh 'node -v'
          }
       }
    }
}