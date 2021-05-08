node('windows-node') {
   def mvnHome
   stage('Preparation') { 
      
      git 'https://github.com/devopsguru91/simple-maven-project-with-tests'
                
      mvnHome = 'C:\\Users\\Administrator\\Downloads\\apache-maven\\apache-maven-3.8.1'
   }
   stage('Build') {
      
         bat "${mvnHome}\\bin\\mvn clean package"
      
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
