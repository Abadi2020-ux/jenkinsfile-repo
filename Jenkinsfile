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
 bat 'newman run C:\\postman-collections\\cicd-collection.postman_collection.json --disable-unicode'
 }
 }
 }
 }
 
