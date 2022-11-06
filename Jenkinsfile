pipeline{
  agent any
  environment{
    Version = "10.2.3"
  }
  parameters{
    string(name:'Version', defaultValue:'', description:'dep')
  }
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
