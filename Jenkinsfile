@Library('piper-lib-os') _

node() {
  stage('init') {
    deleteDir()
    checkout scm
  }
  stage('integrationArtifactDownload Command') {
  //  integrationArtifactDownload script: this
   
 withCredentials([string(credentialsId: 'github-token-san', variable: 'github-token-san')]) {
           sh 'cd $WORKSPACE'
        sh 'git checkout main'
       sh 'git log'
        sh 'touch test.txt'
         sh 'git add ./test.txt'
         sh 'git commit -m test'
   sh 'git push'

      }
     
  }
}
