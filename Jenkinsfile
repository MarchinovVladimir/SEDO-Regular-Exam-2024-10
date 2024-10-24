pipeline {
    agent any 
    stages {
        stage('Restoring dependencies') { 
            steps {
                bat 'dotnet restore' 
            }
        }
        stage('Build') { 
            steps {
                bat 'dotnet build --no-restore' 
            }
        }
        stage('Test') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal' 
            }
        }
    }
}