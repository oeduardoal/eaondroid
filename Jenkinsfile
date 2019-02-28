pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'cmd.exe \'""gradlew.bat"\' clean && exit %%ERRORLEVEL%%"'
        sh 'cmd.exe \'""gradlew.bat"\' assembleDebug && exit %%ERRORLEVEL%%"'
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