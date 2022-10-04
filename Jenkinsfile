pipeline {
   
    agent any
    environment {
    PATH="/opt/homebrew/Cellar/maven/3.8.6/libexec:$PATH"
  }

    stages {
        stage('checkout') {
            steps {
                checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], gitTool: 'Default', userRemoteConfigs: [[url: 'https://github.com/arjitautomation/careerit-mavenrepo.git']]]
            }
        }
        stage('maven build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
