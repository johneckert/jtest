pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENTS', choices: ['jtest-env1', 'jtest-env2'], description: 'Choose Environments to deploy to')
    }
    stages {
        stage ('Deploy') {
            agent {
                label "${params.ENVIRONMENTS}"
            }
            steps {
                echo "Deploying to: ${params.ENVIRONMENTS}"
            }
        }
    }
}