@Library('piper-lib-os') _

//method 1
node() {
  stage('init') {
    deleteDir()
    checkout scm
       sh 'echo $test'
  }
  stage('integrationArtifactDownload Command') {
    //arpit iflow is deployed
   integrationArtifactDownload script: this
    integrationArtifactUpload script: this
      //sangeetha's iflow deploy
       integrationArtifactDeploy script: this 
      //arpits's iflow undeploy
      integrationArtifactUnDeploy script: this 
  
   /* withCredentials([gitUsernamePassword(credentialsId: 'github-token-san', gitToolName: 'Default')]) {
        sh 'cd $WORKSPACE'
        sh 'git checkout main'
        sh 'git add ./iflows/new_flow.zip'
        sh 'git commit -m test'
        sh 'git push'

       }*/
     
   
  }
}
