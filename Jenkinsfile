pipeline {
   agent any
   stages {
   stage('Checkout') {
   steps {
   dir('cicd-pipeline-gradle') {
   git credentialsId: 'GITHUB', url: 'https://github.com/RPraanesh/sample-code-java'
                               }
                     }
            }
   stages {
   stage ('Build') {
     steps {
    echo 'Running Build Automation '
    sh './gradlew build --no-daemon'
    archiveArtifacts artifacts: 'dist/sampleapp.zip'
           }
       }
    }
  }
}
