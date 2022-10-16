def gv

pipeline {
    agent { 
        node {
            label 'jenkins-agent-goes-here'
            }
      }
    stages {
        stage('Init') {
            steps {
                script{
                    gv = load "script.groovy"
                }
            }
        }
        stage('Build') {
            steps {
                script{
                    gv.buildApp()
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    gv.testApp()
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    gv.deployApp()
                }
            }
        }
    }
}
