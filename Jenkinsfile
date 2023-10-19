node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv(installationName: 'SonarServer') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}