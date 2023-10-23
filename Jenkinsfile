pipeline {
  agent any
    stages {
      stage('Build'){
        steps{
          sh "docker build -t adrian734/pokedex-flask:${env.BUILD_NUMBER} ."
      }
    }
  }
}
