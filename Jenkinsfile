pipeline{
    agent any
    stages{
        stage('Maven Compile'){
            steps{
                echo 'Project compile Stage'
                bat label:'Compilation Running',script: '''mvn compile'''
            }
        }
        stage('Unit test'){
            steps{
                echo 'Project Testing Stage'
                bat label:'Test Running',script: '''mvn test'''
            }
        }
        stage('Maven Package'){
            steps{
                echo 'Project packaging Stage'
                bat label:'Project Packaging',script: '''mvn package'''
            }
        }
    }
}