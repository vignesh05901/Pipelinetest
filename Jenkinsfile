node{
  def mvnHome = tool name: 'Maven', type: 'maven'
  stage('Git Checkout'){
    git 'https://github.com/vignesh05901/Pipelinetest'
    }
  stage('Clean'){
  // Get Maven home path
    bat "${mvnHome}/bin/mvn clean"
  
  }
   stage('Verify'){
  // Get Maven home path
    bat "${mvnHome}/bin/mvn verify"
  
  }
    stage('Package'){
  // Get Maven home path
    bat "${mvnHome}/bin/mvn package"
  
  }
}
