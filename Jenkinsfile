pipeline {
  agent any
  
  tools {
    git 'Git'
    maven 'Maven'
  }
  
  stages {
      stage('Git clone') {
          steps {git credentialsId: '1f056d4a-8cbc-425b-a019-be2925f74cac', url: 'https://github.com/dianabala/panda-DB-pub'}
      }
  stage('mvn clean install') {
      steps {sh label: '', script: '''cd mvn
      mvn clean install'''
      }
    }
  }
}
