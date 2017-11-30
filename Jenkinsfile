node {
   def mvnHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/gitforfree/MyProj.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = /usr/share/maven
   }
   stage('Build') {
      // Run the maven build
      
         sh "'${mvnHome}/bin/mvn' clean install"
   }
   
   stage('Publish') {

     nexusPublisher nexusInstanceId: '13.229.109.9', nexusRepositoryId: 'PIPE', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: '/Myprojects/obss-sdlc/targets/obss-proj.war']], mavenCoordinate: [artifactId: 'obss-proj', groupId: 'org.jenkins-ci.main', packaging: 'war', version: '2.23']]]

   }

   }
