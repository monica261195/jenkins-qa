pipeline {
  agent any
  stages {
    stage('Build") {
          when {
            expression {
              env.BRANCH_NAME == 'master' || env.BRANCH_NAME == 'branch1'
                }
                       }
          steps {
            echo "Hi"
                }
                  }
          }
      }
