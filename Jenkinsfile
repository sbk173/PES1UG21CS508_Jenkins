pipeline{
  agent any
  stages {
    stage('Build'){
          steps {
            sh 'make -C main'
            echo "Build Stage Successfull"
          }
    }

    stage('Test'){
          steps {
            echo "Output: ${output}"
            sh './hello_exec'
            echo "Test Stage Successfull"
          }
    }

  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
