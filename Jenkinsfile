pipeline{

agent any

stages{

    stage("git checkout"){
        step {
        checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], gitTool: 'Default', userRemoteConfigs: [[url: 'https://github.com/arjitautomation/careerit-mavenrepo.git']]]
        }
    }
}


}
