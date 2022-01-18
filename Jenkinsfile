pipeline {
  agent any
  stages {
    stage('clonegit') {
      steps {
        git(url: 'https://github.com/QHuyNguyen/Jenkins.git', branch: 'master')
      }
    }

    stage('') {
      steps {
        withAnt(installation: 'ant_1') {
          sh 'ant clean junit'
        }

      }
    }

    stage('testing') {
      steps {
        junit 'test/results/*.xml'
      }
    }

  }
}
