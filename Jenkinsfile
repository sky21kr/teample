pipeline {
  agent any
  stages {
    stage("Build") {
      steps {
        dir("frontend/teampl") {
          sh "sudo npm install"
          sh "sudo npm run build"
        }
      }
    }
    stage("Deploy") {
      steps {
        sh "sudo rm -rf /var/www/jenkins-react-app"
        sh "sudo cp -r ${WORKSPACE}/build/ /var/www/teampl/"
      }
    }
  }
}
