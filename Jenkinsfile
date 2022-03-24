pipeline {
    agent any
    stage('Deploy') {
      steps {
        script {
          docker.withRegistry(
            'https://243833905560.dkr.ecr.us-east-1.amazonaws.com/jenkins-pipeline',
            'arn:aws:ecr:us-east-1:243833905560:repository/jenkins-pipeline'
          ) {
            def myImage = docker.build('jenkins-pipeline')
            myImage.push('image')
          }
        }
          }
        }
    }
}
