node{
  stage('SCM checkout'){
    git 'https://github.com/padhymrutyu/simple-java-project'
  }
  stage('Compile-Package'){
    def mvnhome = tool name: 'maven-3', type: 'maven'
    sh "${mvnhome}/bin/mvn package"
  }
}
