#!groovy

node('master') {
    stage('Checkout') {
        checkout scm
    }
    
    stage('Run tests') {
      withMaven(maven: 'Maven_3.5.2') {
          dir('DEC2019POMSeries') {
            sh 'mvn clean test'
          }
      }
    }
}