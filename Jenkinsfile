pipeline{
  agents any
  stages {
    stage('Build'){
          steps {
            sh 'make -C main'
            echo "Build Stage Successfull"
          }
    }

    stage('Test'){
          steps {
            def output = sh(script: './hello_exec', returnStdout: true).trim()
            echo "Output: ${output}"
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
