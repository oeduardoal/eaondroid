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
        bat(script: 'gradlew', encoding: 'clean', label: 'clean')
        bat 'gradlew'
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