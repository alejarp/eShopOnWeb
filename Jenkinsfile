import groovy.json.JsonSlurperClassic

def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline {
 agent any
     docker {
            image 'maven:3.8.1-jdk-11' // imagen Docker necesaria
            args '-v /var/run/docker.sock:/var/run/docker.sock' // monta el socket Docker
        }
 stages {

 stage("paso 1"){
     
      steps {
          script {			
           sh "docker --version"
        }
      }
    }
  }
  post {
      always {          
          deleteDir()
           sh "echo 'fase always'"
      }
      success {
            sh "echo 'fase success'"
        }

      failure {
            sh "echo 'fase failure'"
      }
      
  }
}  
