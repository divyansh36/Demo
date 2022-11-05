pipeline{
  agent any
    stages{
      stage("run frontend"){
        steps{ 
          echo 'execute yarn!' 
          nodejs("Nodejs-10.17"){
            sh "yarn install"
          }
        }
    }
      stage("run backend"){
        steps{ 
          echo 'run gradle'
          withGralde(){
          sh "./gradlew -v"}
          }
      }
        
    }
  }
