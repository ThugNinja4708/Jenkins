pipeline{
  agent any
  stage("stage-1"){
    steps{
      sh "echo step 1"
    }
  }
  stage("stage-2"){
    when{
      branch 'main'
    }
    steps{
      sh "echo step-2 in main"
    }
    when{
      branch 'preProd'
    }
    steps{
      sh 'echo step-2 in preProd branch'
    
    }
  }
 
}
