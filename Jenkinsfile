pipeline
 {
 agent any
 stages{
 stage('Build Application'){
 steps{
 bat 'mvn clean install'
 }
 }
 
 
  stage('Deploy Application To Mulesoft CloudHub'){
steps{ 
bat 'mvn package deploy -DmuleDeploy'
 }
 }
 
  stage('Perform Regression Testing'){
 steps{
 bat 'C:\\Users\\abadi\\AppData\\Roaming\\npm\\newman run C:\\postman-collections\\git-pipeline-deployment.postman_collection.json --disable-unicode'
 }
 }
 }
 }
 
