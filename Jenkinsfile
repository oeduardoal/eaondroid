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
        bat(script: 'gradlew.bat clean', label: 'clean')
        bat(script: 'gradlew.bat assembleDegub', label: 'gradlew.bat assembleDegub')
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