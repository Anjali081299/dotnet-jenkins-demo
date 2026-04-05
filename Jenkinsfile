pipeline {
    agent any

    stages {

        stage('Checkout') {
    steps {
        git branch: 'main', url: 'https://github.com/Anjali081299/dotnet-jenkins-demo.git'
    }
}

        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build') {
            steps {
                bat 'dotnet build --configuration Release'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }

        stage('Publish') {
            steps {
                bat 'dotnet publish -c Release -o publish'
            }
        }
    }
}
