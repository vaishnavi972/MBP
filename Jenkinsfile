node('master') 
{
    stage('ContinuousDownload') 
    {
       git 'https://github.com/vaishnavi972/maven.git'
    }
    stage('ContinuousBuild') 
    {
       sh 'mvn package'
    }
    stage('ContinuousDeployment') 
    {
       sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.30.8:/var/lib/tomcat8/webapps/testapp.war'
    }
}
