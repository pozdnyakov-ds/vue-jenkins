#!groovy
properties([disableConcurrentBuilds()])

pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        timestamps()
    }
    stages {
        stage("First step") {
            steps {
                sh 'ssh dimon@10.15.6.28 \'hostname\''
            }
        }
        stage("Second step") {
            steps {
                sh 'ssh dimon@10.15.6.28 \'uptime\''
            }
        }
    }
}