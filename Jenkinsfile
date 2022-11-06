pipeline{
  agent any
  tools{
  gradle 'Gradle-6.2'
  }
    stages{
      stage("run frontend"){
        steps{ 
          echo 'execute yarn!' 
          nodejs("NodeJs-10.17"){
            sh "yarn install"
          }
        }
    }
      stage("run backend"){
        steps{ 
          echo "run gradle"
          sh './gradlew -v'}
      }
        
    }
  }
