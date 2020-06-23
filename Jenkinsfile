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
                sh './gradlew build --no-daemon;nohup ./gradlew npm_start &'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
                }}}}
