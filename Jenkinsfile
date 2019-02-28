pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh './gradlew clean'
        sh './gradlew assembleDegub'
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