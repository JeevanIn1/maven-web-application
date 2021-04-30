node
{
def mavenhome = tool name: "maven3.6.2"
timestamps {
    // some block
}
stage('Checkout code')   
{  
git branch: 'development', credentialsId: '9b1271a5-cd9e-46c4-b553-be66a94c2341', url: 'https://github.com/JeevanIn1/maven-web-application.git'  
 }
 stage('build') 
 {
  sh "${mavenhome}/bin/mvn clean package"
 }
 /*
 stage('Upload Artifacts in Repository Nexus')
 {
     sh "${mavenhome}/bin/mvn clean deploy"
 }
 */
 stage ('sending Email Notifications')
 {
     mail bcc: '', body: '''Here it it is first Job

With Regards 
Jeevan''', cc: 'avinashreddyd166@gmail.com', from: '', replyTo: '', subject: 'Job Mail', to: 'jeevanpvrpl@gmail.com'
 }
}  
    
