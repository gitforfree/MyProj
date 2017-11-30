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
      
         sh "mvn clean deploy"
   }
   
   }
