pipeline {
    agent { docker { image 'python:3.7.3' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('Linting') { // Run pylint against your code
            steps {
                script {
                  sh """
                  pylint **/*.py
                  """
                }
            }
        }
    }
}
