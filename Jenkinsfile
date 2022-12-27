@Library('piper-lib-os') _

node() {
  stage('init') {
    deleteDir()
    checkout scm
       sh 'echo $test'
  }
  stage('integrationArtifactDownload Command') {
    integrationArtifactDeploy script: $test
 
  /* withCredentials([gitUsernamePassword(credentialsId: 'github-token-san', gitToolName: 'Default')]) {
        sh 'cd $WORKSPACE'
        sh 'git checkout main'
        sh 'git add ./iflows/new_flow.zip'
        sh 'git commit -m test'
        sh 'git push'
  integrationArtifactUpload script: this
  integrationArtifactDeploy script: this 
 
      }
      */
  }
}
