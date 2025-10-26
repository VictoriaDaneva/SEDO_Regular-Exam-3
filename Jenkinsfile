pipeline{
    agent any
    stages{
        stage("Restore .NET Packages"){
            steps{
                bat 'dotnet restore'
            }
        }
        stage("Build .NET Project"){
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Run Unit and Integration tests in .NET Project"){
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}