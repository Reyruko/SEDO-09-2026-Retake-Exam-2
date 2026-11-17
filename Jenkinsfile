pipeline {
    agent any

    stages {
        stage('Restore Dependencies') {
            steps {
                bat 'dotnet restore Homies.sln'
            }
        }

        stage('Build Application') {
            steps {
                bat 'dotnet build Homies.sln --no-restore'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'dotnet test Homies.sln --no-build'
            }
        }
    }
}