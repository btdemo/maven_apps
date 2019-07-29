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
   
   stage('sonar test') {
      withMaven(jdk: 'JDKv8', maven: 'Maven'){
    sh 'mvn sonar:sonar +
  -Dsonar.projectKey=maven-apps +
  -Dsonar.organization=btdemo +
  -Dsonar.host.url=https://sonarcloud.io +
  -Dsonar.login=de1c489b23ff123c938d9d07031f5d01f2ca2bd6'
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

