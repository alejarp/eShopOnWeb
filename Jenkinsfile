pipeline {
  agent { label 'main' }
  environment {
    appName = "variable" 
  }
  agent any
  stages {

 stage("paso 1"){
     
      steps {
          script {			
           sh "echo 'hola mundo'"
        }
      }
    }
  }
}
