pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        node {
          label 'context'
        }

      }
      steps {
        sh 'cmd.exe /C "gradlew.bat clean"'
        sh 'cmd.exe /C "gradlew.bat assembleDebug"'
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