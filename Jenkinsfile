pipeline{
  agent any

  stages {
    stage ('prepare the  Artifact') {
      steps{
       sh '''
         zip -r ../todo.zip *
       '''
      }
    }
    stage('upload the artifact in to nexus'){
      steps{
        sh '''
           curl -f -v -u admin:admin123 --upload-file ../todo.zip http://172.31.10.228:8081/repository/todo/todo.zip

        '''

      }

    }

  }
}