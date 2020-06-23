pipeline {
    agent any
    stages {
        stage('git'){
          steps{
            git 'https://github.com/balucc/train-app.git'
            }}
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
                }}}}
