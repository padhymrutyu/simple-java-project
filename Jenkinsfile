node{
  stage('SCM checkout'){
    git 'https://github.com/padhymrutyu/simple-java-project'
  }
  stage('Compile-Package'){
    def mvnhome = tool name: 'maven-3', type: 'maven'
    sh "${mvnhome}/bin/mvn clean package"
  }
  stage('SonarCube Analysys'){
    def mvnhome = tool name: 'maven-3', type: 'maven'
    withSonarQubeEnv(credentialsId: 'sonar1') {
     sh "${mvnhome}/bin/mvn sonar:sonar"
    }
  }
  stage('Email Notification'){
    mail bcc: '', body: '''hello welcome to jenkins email alert
thanks
subham''', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'mrutyunjayapadhy25@gmail.com'
  }
}
