pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENTS', choices: ['jtest-env1', 'jtest-env2'], description: 'Choose Environments to deploy to')
    }
    stages {
        stage ('Checkout Code to temp file') {
            agent any
            steps {
                //check out code
                git 'https://github.com/johneckert/jtest.git'
            }
        }

        stage ('Build Project UI') {
            steps {
                sh 'npm install'
                
            }
        }
    }
}