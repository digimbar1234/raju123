node{
   stage('scm-checkout'){
     git 'https://github.com/digimbar1234/raju123'
   }
   stage('compile-package'){
      def mvnHome = tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email notification'){
      mail bcc: '', body: '''hi
      welcome to jenkins''', cc: '', from: '', replyTo: '', subject: 'jenkins job', to: 'mallick.digambar@gmail.com'
   }
   
}   
   
