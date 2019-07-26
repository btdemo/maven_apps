node {
   
   stage('checkoutcode') { 
       git credentialsId: 'Git', url: 'https://github.com/btdemo/maven_apps.git'
       
   }
   stage('Build') {
       withMaven(jdk: 'JDK8.0', maven: 'Maven 3.6') {
    sh 'mvn clean compile'
}
      
   }
   stage('unit test') {
       withMaven(jdk: 'JDK8.0', maven: 'Maven 3.6') {
    sh 'mvn test'
}
     
     
   }
   stage('package') {
       withMaven(jdk: 'JDK8.0', maven: 'Maven 3.6') {
    sh 'mvn package'
}
     
     
   }

    stage('deploy to Dev Env.') {
     
     
   }
   stage('deploy to Test Env.') {
     
     
   }
   stage('deploy to Prod Env.') {
     
     
   }
    
}

