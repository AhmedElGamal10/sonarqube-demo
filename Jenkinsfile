node {
  stage('SC Checkout') {
    git 'https://github.com/AhmedElGamal10/sonarqube-demo.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('LocalSonar') {
      sh './mvnw clean package sonar:sonar -Dsonar.host.url=http://localhost:9000'
    }
  }
}