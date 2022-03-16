pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the first job compile'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the second job test'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the third job package'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this is first pipeline by code...'
    }

  }
}