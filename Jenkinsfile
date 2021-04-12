pipeline{
  agent any
  stages{
    stage("git checkout"){
      steps{
        script{
          sh """
          git clone https://github.com/ravi1312/Jenkinsjob.git
          git checkout master
          """
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
