pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        // Perform your build steps here
        sh 'echo "Building..."'
      }
    }

    stage('Test') {
      steps {
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
        subject: "github Jenkins Pipeline task by vishal",
        body: "The pipeline has completed successfully.",
        to: "rajesh3390@gmail.com",
        replyTo: "rajesh3390@gmail.com"
      )
    }
  }
}
