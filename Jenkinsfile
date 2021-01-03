node{
  stage('SCM checkout'){
    git 'https://github.com/padhymrutyu/simple-java-project'
  }
  stage('Compile-Package'){
   sh 'mvn package'
  }
}
