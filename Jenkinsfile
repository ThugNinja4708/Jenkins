pipeline {
  agent any
  stages {
    stage('Example Build') {
      steps {
        sh 'echo Hello World'
      }
      input {
        message "What is your first name?"
        ok "Submit"
        parameters {
          string(defaultValue: 'Dave', name: 'FIRST_NAME', trim: true) 
        }
      }
    }
    stage('Example Deploy') {
      when {
        branch 'main'
      }
      steps {
        sh 'echo main branch'
      }
    }
  }
}
