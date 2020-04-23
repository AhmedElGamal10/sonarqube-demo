node {
  stage('SCM') {
    git 'https://github.com/AhmedElGamal10/sonarqube-demo.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('LocalSonar') {
      sh 'mvn clean package sonar:sonar'
    }
  }
}