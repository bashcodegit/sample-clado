pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        sh 'echo Build......'
      }
    }
    stage("Test"){
      steps{
        sh 'echo Testing.....'
      }
    }
    stage("Sonar Analysis"){
      steps{
        def scannerHome = tool 'SonarScanner';
        withSonarQubeEnv() {
          sh "${scannerHome}/bin/sonar-scanner"
      }
    }
  }
}
