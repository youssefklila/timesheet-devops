pipeline {
    agent any

    stages {
        stage('Récupération du code de la branche') {
            steps {
                git branch: 'master',
                url: 'https://github.com/youssefklila/timesheet-devops.git'
            }
        }
    }
    
      stage('Nettoyage et compilation avec Maven') {
            steps {
                // Étape de nettoyage du projet
                sh "mvn clean"

                // Étape de compilation du projet
                sh "mvn compile"
                // Etape de sonar
            }
        }
}
