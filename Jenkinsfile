node
{
stage('clone the code'){
git 'https://github.com/skalikhan/one.git'
}
stage('build the code'){

sh "mvn clean package"
}
stage('artifact deployment')
{
sshagent(['43bb33d6-7bc8-4552-a7c5-283c23405b13']) {
    sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Pipeline_proj/target/myproj.war ubuntu@ip-172-31-40-216:/opt/apache-tomcat-10.1.28/webapps/"  
}

}
}
