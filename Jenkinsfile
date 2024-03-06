pipeline{
  agent any
  stages {
    stage('Build'){
          steps {
            sh 'make -C main'
            echo "Build Stage Successful"
          }
    }

    stage('Test'){
          steps {
            echo "Output:"
            sh './hello_exec.exe'
            echo "Test Stage Successful"
          }
    }

  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
