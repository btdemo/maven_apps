node {
   
   stage('checkoutcode') { 
git credentialsId: 'git', url: 'https://github.com/btdemo/maven_apps.git'       
   }
   stage('Build') {
      withMaven(jdk: 'JDKv8', maven: 'Maven'){
         sh 'mvn clean compile'
}
      
   }
   stage('unit test') {
      withMaven(jdk: 'JDKv8', maven: 'Maven'){
    sh 'mvn test'
}
     
     
   }
   stage('package') {
      withMaven(jdk: 'JDKv8', maven: 'Maven'){
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

