pipeline {
    agent any

    stages {
        stage('frontend') {
            steps {
                echo 'executign yarn...'
                nodejs('Node-10.17') {
                sh 'yarn install'
            }
        }
     }
        stage('run backend') {
            steps {
                echo 'executign gradle....'
                withGradle() {
                sh './gradelw -v'
                }       
            }
        }
    }
}
