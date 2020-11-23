node{
   def mvnHome
   stage('Preparation'){
       git 'https://github.com/SouhardyaDas/JenkinsDemo.git'
       mvnHome = tool 'MAVEN_HOME'
    }
   stage('Build'){
      withEnv(['%MAVEN_HOME%=$mvnHome']){
           bat(/"%MAVEN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package 
pause/)
      }
   }
}
