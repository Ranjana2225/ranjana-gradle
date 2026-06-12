pipeline{
  agent any
    tools{
      gradle 'Gradle'
        jdk 'jdk'
    }
    stages{
      stage('checkout'){
        steps{
          git branch:'master',
            url:'https://github.com/Ranjana2225/ranjana-gradle.git'
        }
        }
      stage('Build'){
        steps{
          sh 'gradle build'
        }
      }
      stage('test'){
        steps{
          sh 'gradle test'
        }
      }
        stage('Run application'){
          steps{
            sh 'gradle run'
          }
        }
      }
 post{
   success{
     echo 'Build successful'
   }
   failure{
     echo 'Build failed'
   }
 }
 }
        
        
