pipeline {
  agent any 
  parameters {
    choice(name : 'VERSION' , choices : ['1.1.0','1.2.0','1.3.0','1.4.0'] , description: 'Select Version')
    booleanParam(name: 'executeTests' , defaultValue: true , description : 'Skip Tests?')
    }
    stages {
      stage ("build") {
        steps {
          echo 'building the app'
          }
         }
         stage("test") {
         when {
          expression {
            params.executeTests
            }
            }
         steps {
          echo 'testing the application'
          }
          }
          stage("deploy"){
          steps { 
            echo ' deploying the app'
            echo " deploying the version ${params.VERSION}"
            }
            }
            }
            }
