pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        sh "docker build -t adrian734/pokedex-flask:${env.BUILD_NUMBER} ."
      }
    }
    
    stage('Login to Dockerhub'){
        steps{
            sh "echo $DOCKERHUB_CREDENCIALS_PSW | docker login -u $DOCKERHUB_CREDENCIALS_USR --password-stdin "
        }
    }

    stage('Push image to Dockerhub'){
        steps{
            sh "docker push ${env.RepoDockerHub}/${env.NameContainer}:${env.BUILD_NUMBER} "
        }
    }
  }
}
