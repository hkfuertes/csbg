pipeline {
  agent any
  stages {
    stage('Jekyll') {
      environment {
        JEKYLL_ENV = 'docker'
      }
      steps {
        sh 'docker run --rm --volumes-from jenkins-docker -w ${WORKSPACE} jekyll/jekyll jekyll build --config _config.docker.yml'
      }
    }

    stage('Publish') {
      parallel {
        stage('Publish') {
          steps {
            sh 'tar -zcvf ${WORKSPACE}/csbook_guides_${BUILD_NUMBER}.tgz -C ${WORKSPACE}/_site .'
            archiveArtifacts 'csbook_guides_${BUILD_NUMBER}.tgz'
          }
        }

        stage('SSH') {
          steps {
            sh 'ssh credentials(\'CSBOOK\')@csbook.es rm -rf /home/hkfuertes/csbg_jenkins/'
            sh 'ssh hkfuertes@csbook.es mkdir /home/hkfuertes/csbg_jenkins/'
            sh 'scp -r _site hkfuertes@csbook.es:/home/hkfuertes/csbg_jenkins'
          }
        }

      }
    }

  }
}