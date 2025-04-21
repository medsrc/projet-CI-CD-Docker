pipeline {
    agent any
     tools {
           maven "maven"
     }
      stages {
        stage('cleanUp') {
            steps {
                deleteDir()
                  }
        }
        stage('Checkout SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/medsrc/projet-CI-CD-Docker.git'
                  }
        }
         stage('Build') {
             steps {
                    sh "mvn clean install"
                   }
       }
    }
}
