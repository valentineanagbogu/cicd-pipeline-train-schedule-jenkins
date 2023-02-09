pipeline {
  agent any
  properties([pipelineTriggers([githubPush()])])
        node {
        git url: 'https://github.com/valentineanagbogu/cicd-pipeline-train-schedule-jenkins.git',branch: 'master'
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        }
      }
    } 
  }
}
