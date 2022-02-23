pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'df -Th'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            archiveArtifacts(caseSensitive: true, artifacts: 'newfile.txt')
          }
        }

        stage('error') {
          steps {
            echo 'nothing'
          }
        }

      }
    }

  }
}