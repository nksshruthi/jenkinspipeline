pipeline {
  agent any
  stages {
    stage('plan') {
      steps {
        echo 'plans for pipeline'
      }
    }

    stage('code') {
      steps {
        echo 'prepare code for pipeline'
      }
    }

    stage('build') {
      steps {
        echo 'build code for pipeline'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test code for pipeline'
          }
        }

        stage('release') {
          steps {
            echo 'release code for pipeline'
          }
        }

        stage('operate') {
          steps {
            echo 'operate code for pipeline'
          }
        }

        stage('deploy') {
          steps {
            echo 'deploy code for pipeline'
          }
        }

      }
    }

    stage('end') {
      steps {
        echo 'end'
      }
    }

  }
}