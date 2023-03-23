pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Git Checkout'
      }
    }

    stage('Build') {
      steps {
        echo 'Build ops'
      }
    }

    stage('Quality Check') {
      parallel {
        stage('Quality Check') {
          steps {
            echo 'Quality checking'
          }
        }

        stage('Integration Tests') {
          steps {
            echo 'integration tests'
          }
        }

        stage('SonarQube Analysis') {
          steps {
            echo 'sonar analysis'
          }
        }

        stage('Unit Tests') {
          steps {
            echo 'quality gate checking'
          }
        }

      }
    }

    stage('Quality Gate Control') {
      steps {
        echo 'gate control'
      }
    }

    stage('Performance Analysis') {
      steps {
        echo 'performance analysis'
      }
    }

    stage('Register Image') {
      steps {
        echo 'image'
      }
    }

    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }

  }
}