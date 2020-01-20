node {
    
    stages {
     stage 'checkout'
     git url: 'https://github.com/Mohini-Dangale/jenkins_pipeline.git'
     
     def mvnHome = tool 'M3'
     
     stage 'Build'
   // Run the maven build
   sh "${mvnHome}/bin/mvn clean sonar:sonar"
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
   
   }
   }
