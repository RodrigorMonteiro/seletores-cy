pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                git branch: 'main', url: 'https://github.com/RodrigorMonteiro/seletores-cy.git'
                sh 'npm install'
                sh 'npm install cypress --save-dev'
            }
        }
        stage('Test') {
            steps {
                sh 'NO_COLOR=1 npm test'
            }
        }
    }
}
