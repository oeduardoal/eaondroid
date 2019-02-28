pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'gradlew.bat clean'
        sh 'gradlew.bat clean'
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