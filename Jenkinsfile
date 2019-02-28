pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        powershell './gradlew clean'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts '**/*.apk'
      }
    }
  }
  environment {
    ANDROID_HOME = 'C:\\Users\\7700274224\\AppData\\Local\\Android\\Sdk'
  }
}