pipeline {
  agent any
  stages {
    stage('Clonar Repo') {
      steps {
        git url: 'https://github.com/Sankyor/desafiolatam-TechFlow.git', branch: 'main'
      }
    }
    stage('Instalar Dependencias') {
      steps {
        sh 'npm install' // Cambia de 'npm ci' a 'npm install'
      }
    }
    stage('Pruebas') {
      steps {
        sh 'npm run test'
      }
    }
    stage('Construir Docker') {
      steps {
        sh 'docker build -t techflow-api .'
      }
    }
  }
}