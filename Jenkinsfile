@Library('piper-lib-os') _

node() {
  stage('init') {
    deleteDir()
    checkout scm
  }
  stage('integrationArtifactDownload Command') {
    integrationArtifactDownload script: this
   
 withCredentials([string(credentialsId: 'cpi-git-access-token', variable: 'cpi-git-access-token')]) {
         sh 'git checkout main'
         sh 'git add ./iflows/*.zip'
         sh 'git commit -m test'
         sh 'git push'
      }
     
  }
}
