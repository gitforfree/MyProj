node {
   
   stage('source') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/gitforfree/MyProj.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      
   }
   stage('Build') {
      // Run the maven build
      
         sh "mvn clean install"
   }
   
   stage('Publish') {

     nexusPublisher nexusInstanceId: 'NexusPipeline', nexusRepositoryId: 'PIPE', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: '/var/lib/jenkins/workspace/Pipeline_Jenkinsfile/target/obss-sdlc-0.0.1-SNAPSHOT']], mavenCoordinate: [artifactId: 'obss-proj', groupId: 'org.jenkins-ci.main', packaging: 'war', version: '2.23']]]

   }

   }
