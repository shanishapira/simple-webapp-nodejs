pipeline {
    agent any

    stages {

        stage('cleanWS') {
            steps {
                cleanWs()
            }
        }

        stage('clone git') {
            steps {
                git 'https://github.com/Elad0109/simple-webapp-nodejs.git'
                
                
            }
        }
        stage('build') {
            steps {
                nodejs('Node8') {
                    sh "npm install"
                }
            }
        }
        stage('test') {
            steps {
                nodejs('Node8') {
                    sh "npm run test"
                }
    
            }

        }

    }
}
