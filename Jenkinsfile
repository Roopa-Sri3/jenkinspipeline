pipeline{
  agent any

  stages{
    stage("Checkout"){
    steps{
      git 'https://github.com/Roopa-Sri3/jenkinspipeline.git'
    }
  }
  stage("Build"){
    steps{
      script{
        sh """
        dotnet restore
        msbuild method2Postgresql.sln
        dotnet build
        """
      
    }
  }
  }
    stage("run"){
      steps{
        
        script{
          sh 'dotnet run'
        }
        
      }
    }
  }
}
    
