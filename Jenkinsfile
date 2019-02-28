pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        node {
          label './'
        }

      }
      steps {
        sh 'sh "cmd.exe /C \\"gradlew.bat clean\\""'
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