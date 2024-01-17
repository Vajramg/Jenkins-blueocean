pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls-la'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test print'
          }
        }

        stage('test print') {
          steps {
            echo 'test par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 12
      }
    }

  }
}