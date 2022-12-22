@Library('piper-lib-os') _

node() {
  stage('init') {
    deleteDir()
    checkout scm
  }
  stage('integrationArtifactDownload Command') {
  //  integrationArtifactDownload script: this
   
// withCredentials([string(credentialsId: 'github-token-san', variable: 'github-token-san')]) 
    
    withCredentials([gitUsernamePassword(credentialsId: 'github-token-san', gitToolName: 'Default')]) {
           sh 'cd $WORKSPACE'
        sh 'git checkout main'
      // sh 'git log'
        sh 'touch test.txt'
         sh 'git add ./test.txt'
         sh 'git commit -m test'
  //sh ' git config --local credential.helper "!f() { echo username=\\$GIT_AUTH_USR; echo password=\\$GIT_AUTH_PSW; }; f"'
    sh 'git push'

      }
     
  }
}
