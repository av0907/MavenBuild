node('Slave1')
{
stage("Code Checkout")
{
checkout([$class: 'GitSCM', branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/av0907/MavenBuild.git']]])
}
}
