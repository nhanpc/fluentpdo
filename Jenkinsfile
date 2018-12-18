pipeline {
  agent any
  stages {
    stage('backup_stage') {
      steps {
        sh 'backup.sh'
      }
    }
    stage('Check_current_status') {
      steps {
        build 'testjob'
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