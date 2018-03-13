library identifier: 'jenkins-lib@master', retriever: modernSCM(
        [$class: 'GitSCMSource',
         remote: 'git@bitbucket.org:brickvest/devops-jenkins.git',
         credentialsId: 'ssh_deploy_key'])
pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"
            }
        }
    }
}
