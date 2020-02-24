pipeline {
  agent any
  stages {
    stage('Jekyll') {
      steps {
        sh '''docker run --rm --volumes-from jenkins-docker --workdir="${WORKSPACE}"  jekyll/jekyll 
  jekyll build --config _config.docker.yml'''
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