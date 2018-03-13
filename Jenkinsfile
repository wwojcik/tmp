library identifier: 'jenkins-lib@master', retriever: modernSCM(
        [$class: 'GitSCMSource',
         remote: 'git@bitbucket.org:brickvest/devops-jenkins.git',
         credentialsId: 'ssh_deploy_key'])
def helm = com.brickvest.jenkins.shared.Helm()
pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage('Example') {
            helm.deploy("ee")
            steps {


                echo "Hello ${params.PERSON}"
            }
        }
    }
}
