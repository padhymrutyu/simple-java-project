node{
  stage('SCM checkout'){
    git 'https://github.com/padhymrutyu/simple-java-project'
  }
  stage('Compile-Package'){
    def mvnhome = tool name: 'maven-3', type: 'maven'
    sh "${mvnhome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''helo welcome to jenkins email alert
thanks 
regards subham''', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'mrutyunjayapadhy25@gmail.com'
  }
}
