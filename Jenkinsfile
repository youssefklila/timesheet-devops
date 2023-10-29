pipeline {
    agent any

    stages {
        stage('Récupération du code de la branche') {
            steps {
                git branch: 'master',
                url: 'https://github.com/youssefklila/timesheet-devops.git'
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
        stage('MVN SONARQUBE'){
        steps {
            sh "mvn sonar:sonar -Dsonar.login=e10380a5a72c7aa2d861f345638de9e85dee25ad"
        }
        }
    }
}
