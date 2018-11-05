pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            echo 'i am test message'
            echo '222222'
          }
        }
        stage('stage3') {
          steps {
            svn(changelog: true, poll: true, url: 'https://192.168.2.101:8443/svn/PlanningManagement/trunk/code/PlanningManagement')
          }
        }
      }
    }
    stage('stage2') {
      steps {
        sh 'dir'
        sleep 2
      }
    }
  }
}