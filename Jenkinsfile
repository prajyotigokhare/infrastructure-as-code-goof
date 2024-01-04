pipeline 
{
    agent any 
     
      stages {
        stage('pull code') {
           steps {
             git credentialsId: '123', url: 'https://github.com/prajyotigokhare/infrastructure-as-code-goof.git'
               }
             }
      stage('Test') {
        steps {
             snykSecurity( snykInstallation: 'snyk', snykTokenId: 'snykid' )
            {
                sh './snyk iac test'
            }
           }  
      }
       }
  }
