pipeline {
    agent any

    stages {
        stage('Clonar o repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/anapmedeiros/TCC-EBAC.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                bat 'cd teste-ui && npm install'
            }
        }
        stage('Executar testes') {
            steps {
                bat 'cd teste-ui && npm run cy:run'
            }
        }
    }
}