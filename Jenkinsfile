pipeline{
    agent any
    stages{
        stage("Checkout"){
            steps{
               git 'https://github.com/Roopa-Sri3/jenkinspipeline.git'
               //sh "cd LoginRegisterFormWithEF_PostgreSQL-master"
        }
        }
        stage("Build"){
            steps{
                 
                 script {
                     sh """
                     dotnet restore
                     dotnet build
                     """
                 }
           }

        }
        stage("Run"){
            steps{
                script{
                    sh """
                    sudo apt upgrade dotnet-sdk-6.0
                    dotnet /var/lib/jenkins/workspace/One/LoginRegisterFormWithEF_PostgreSQL-master/method2Postgresql/bin/Debug/net6.0/method2Postgresql.dll
                    """
                }
            }
        }
    }
}
