pipeline {
    environment {
        registry = "jackcharles13/dndproject"
        registryCredential = 'dockerhub_id'
        dockerImage = ''
        DOCKERHUB_CREDENTIALS=credentials('dockerhub_id')
        }

    agent any
    stages {
      stage('Building image') {
        steps{
            sh 'docker-compose build'
                }
           }

      stage('Deploying image to Dockerhub') {
        steps{
             sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
             sh 'docker push jackcharles13/tem'
                }
           }
           
      stage('ssh into NotesVM') {
        steps{
          sh 'cd /var/lib/jenkins/keys'
          sh 'ssh -i /var/lib/jenkins/.ssh/NotesApp_key.pem azureuser@20.90.186.210'
          sh 'docker pull jackcharles13/tem:latest'
          sh 'exit'
                }
           }     
      }
}
