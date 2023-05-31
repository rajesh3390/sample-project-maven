pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        // Perform your build steps here
        sh 'echo "Building..."'
      }
    }

    stage('Emailresults') {
      steps {
          emailext attachLog: true, attachmentsPattern: '*xml', body: 'assignment', compressLog: true, mimeType: 'text/html', subject: 'GIT hub jenkins pipeline', to: 'rajesh3390@gmail.com, avsvishal94@gmail.com'
        // Perform your testing steps here
        sh 'echo "Testing..."'
      }
    }

    stage('Deploy') {
      steps {
        // Perform your deployment steps here
        sh 'echo "Deploying..."'
      }
    }
  }

  post {
    always {
      // Send email notification to recipients
      emailext (
  subject: 'github Jenkins Pipeline task by vishal',
  body: 'The pipeline has completed successfully.',
  to: 'rajesh3390@gmail.com, avsvishal94@gmail.com',
  replyTo: 'rajesh3390@gmail.com'
)

    }
  }
}
