pipeline {
    agent{
    node {
            label 'docker'
        }
    }
    stages {
            stage('Example Build') {
                steps {
                    sh 'make up'
                }
            }
        }
}
