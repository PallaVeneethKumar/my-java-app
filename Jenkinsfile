pipeline{
  agent any
  stages{
    stage("git checkout") {
      when{
        branch 'test'
      }
steps{
  echo "code checkout"
}
    }
    stage("sonarqube") {
      when{
        branch 'develop'
      }
steps{
  echo "static code anylysis"
}
    }
stage("maven build") {
      when{
        branch 'uat'
      }
steps{
  echo "maven build done"
}
    }
stage("nexus") {
      when{
        branch 'main'
      }
steps{
  echo "uploading artifacts"
}
    }
  }
}
    
