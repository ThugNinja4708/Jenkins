pipeline {
  agent any
  stages {
    stage('Example Build') {
      options {
        timeout(time: 10, unit: 'SECONDS') 
      }

      input {
        message "What is your first name:"
        ok "Submit"
        parameters {
          string(defaultValue: 'Thug', name: 'FIRST_NAME', trim: true) 
        }
      }
      steps {
        sh 'echo Hello World'
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
