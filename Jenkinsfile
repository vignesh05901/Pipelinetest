node{
  def mvnHome = tool name: 'Maven', type: 'maven'
  stage('Git Checkout'){
    git 'https://github.com/vignesh05901/Pipelinetest'
    }
  stage('Clean'){
  // Get Maven home path
    sh "${mvnHome}/bin/mvn clean"
  
  }
   stage('Verify'){
  // Get Maven home path
    sh "${mvnHome}/bin/mvn verify"
  
  }
    stage('Package'){
  // Get Maven home path
    sh "${mvnHome}/bin/mvn package"
  
  }
  stage('Deploy to Tomcat'){
  sshagent(['tomcat-dev']) {
    sh 'scp -o StrictHostKeyChecking=no target/*war ec2-user@172.31.29.233:/opt/tomcat9/webapps/'
}
}
}
