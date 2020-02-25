node{
  stage('Git Checkout'){
    git 'https://github.com/vignesh05901/Pipelinetest'
    }
  stage('Clean'){
  // Get Maven home path
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn clean"
  
  }
    stage('Validate'){
  // Get Maven home path
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn validate"
  
  }
    stage('Package'){
  // Get Maven home path
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  
  }
}
