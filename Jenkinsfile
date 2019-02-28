pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        bat 'gradlew.bat clean'
        bat 'gradlew.bat assembleDebug'
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