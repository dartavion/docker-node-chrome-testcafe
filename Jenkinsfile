#!/usr/bin/env groovy
pipeline {
    agent {
      docker {
          image 'testcafe/testcafe'
      }
    }
    stages {
      stage ('Pre') {
          steps {
              script {
                    checkout scm
                    sh 'npm -v'
                    sh 'node -v'
                    sh 'ls -al'
                    sh 'npm install'
                    sh 'testcafe -b'
                    sh 'which chromium-browser'
                    sh 'npm run testChromeOld'
                }
          }
       }
    }
}