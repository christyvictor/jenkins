pipeline {
    agent any

    stages {
        stage('frontend') {
            steps {
                echo 'executing yarn...'
                nodejs('Node-10.17') {
                sh 'yarn install'
            }
        }
     }
        stage('run backend') {
            steps {
                echo 'executing gradle....'
                withGradle() {
                sh './gradlew -v'
                }       
            }
        }
    }
}
