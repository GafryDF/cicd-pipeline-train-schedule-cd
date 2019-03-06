pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Staging') {
            steps {
                echo 'Staging'
            }
        }
        stage('Production') {
            steps {
                input 'Do you want to proceed?'
                echo 'Production'
            }            
        }        
    }
}
