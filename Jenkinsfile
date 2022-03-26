node('Slave1')
{
stage("Code Checkout")
{
checkout([$class: 'GitSCM', branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/av0907/MavenBuild.git']]])
}
stage("Build")
{
sh '''ls -lart
mvn clean install'''
}
stage("Deploy")
{
deploy adapters: [tomcat9(credentialsId: 'Tomcat_creds', path: '', url: 'http://34.228.59.197:8080/')], contextPath: 'firstapp', onFailure: false, war: 'target/*.war'
}

}
