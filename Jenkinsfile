pipeline{
  agent any
  environment{
    CODE_PATH = '/var/lib/jenkins/workspace/One/LoginRegisterFormWithEF_PostgreSQL-master/method2Postgresql'
  }
  stages{
    stage("Checkout"){
    steps{
      git 'https://github.com/Roopa-Sri3/jenkinspipeline.git'
    }
  }
  stage("Build"){
    steps{
      dir(env.CODE_PATH){
      script{
        sh """
        dotnet restore
        dotnet build
        """
      }
    }
  }
  }
    stage("run"){
      steps{
        dir(env.CODE_PATH){
        script{
          sh 'dotnet run'
        }
        }
      }
    }
  }
}
    
