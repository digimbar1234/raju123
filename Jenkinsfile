node{
   stage('scm-checkout'){
     git 'https://github.com/digimbar1234/raju123'
   }
   stage('compile-package'){
      def mvnHome = tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('SonarQube analysis') {
      def mvnHome = tool name: 'maven-3', type: 'maven'
      withSonarQubeEnv('sonar-6'){
       sh "${mvnHome}/bin/mvn sonar:sonar"
      }   
   }   
   stage('Email notification'){
      mail bcc: '', body: '''hi
      welcome to jenkins''', cc: '', from: '', replyTo: '', subject: 'jenkins job', to: 'mallick.digambar@gmail.com'
   }
   
}   
   
