pipeline {
  agent any
  stages {
    stage('Jekyll') {
      environment {
        JEKYLL_ENV = 'docker'
      }
      steps {
        sh '''docker run --rm --volumes-from jenkins-docker -w "${WORKSPACE}"  jekyll/jekyll 
  jekyll build --config ${WORKSPACE}/_config.docker.yml'''
      }
    }

    stage('Publish') {
      steps {
        sh 'tar -zcvf ${WORKSPACE}/../csbook_guides_${BUILD_NUMBER}.tgz *'
        sh 'mv ${WORKSPACE}/../csbook_guides_${BUILD_NUMBER}.tgz ${WORKSPACE}/csbook_guides_${BUILD_NUMBER}.tgz'
        archiveArtifacts 'csbook_guides_${BUILD_NUMBER}.tgz'
      }
    }

  }
}