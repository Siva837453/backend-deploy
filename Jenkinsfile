pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit:'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
    parameters {
        string(name: 'appVersion', defaultValue: '1.0.0', description: 'What is the application version?')
    }
    environment{
        def appVersion = '' //variable declaration
        nexusUrl = 'nexus.sdevops.cloud:8081'
    }
  
    stages {
        stage('Deploy'){
            steps{
                script{
        
                    echo "application version: ${params.appVersion}"
                }
            }
        }
        
               
    }
          
    post{
        always{
            echo " i will always say hellow again"
            //deleteDir()
        }
        success{
            echo " i will run when pipeline is success"
        }
        failure{
            echo " i will run when pipeline is failure"
        }
    }
}
