pipeline {
    agent {
        label 'nop'

    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('scm') {
            steps {
                git url: 'https://github.com/sangameshwar-0109/jenkis-202.git',
                    branch: 'develop'
            }
        }
        stage('build') {
            steps {
                sh 'dotnet publish -o published/ -c Release src/Presentation/Nop.Web/Nop.Web.csproj'
            }

        }
        
    }
}
