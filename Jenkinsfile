pipeline {
  agent any
  stages {
    stage('backup_stage') {
      steps {
        sh 'echo hello'
      }
    }
    stage('Check_current_status') {
      parallel {
        stage('Check_current_status') {
          steps {
            build 'testjob'
          }
        }
        stage('xx') {
          steps {
            sleep 4
          }
        }
      }
    }
    stage('Merge') {
      steps {
        git(url: 'merge master', branch: 'master')
      }
    }
    stage('Pull') {
      steps {
        git 'sss'
      }
    }
    stage('Final test') {
      steps {
        build 'ed test'
      }
    }
  }
}