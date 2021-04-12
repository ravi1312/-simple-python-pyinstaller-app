pipeline{
  agent any
  stages{
    stage("git checkout"){
      steps{
        script{
          try {
            sh """
            git clone https://github.com/ravi1312/Jenkinsjob.git
            git checkout master
            """
          }
          catch (e){
            echo "fatal error"
            error ('*******FATAL ERROR*********')
          }
        }
      }
    }
    stage("testing"){
      steps{
        script{
          sh """
          cd $WORKSPACE/Jenkinsjob
          ls
          """
        }
      }
    }
  }
  post{
    always{
      echo "cleaning up workspace"
    }
  }
}
