pipeline{

agent any

stages{

    stage("git checkout"){
    step{
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], gitTool: 'Default', userRemoteConfigs: [[url: 'https://github.com/arjitautomation/careerit-mavenrepo.git']]])
    }})
}


}
