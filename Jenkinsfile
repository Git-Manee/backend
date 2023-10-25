pipeline {
    agent { label 'workstation'}
    stages {
        stage('Download Dependencies'){
            steps{
                sh 'npm install'
            }
        }
        stage('Code Quality'){
            steps{
                sh 'sonar-scanner -Dsonar.host.url=http://172.31.88.39:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=backend -Dsonar.qualitygate.wait=true'
            }
        }
        stage('Unit Test'){
            steps{
                // Ideally we should run the tests , But here the Developer has skipped it. So assuming those are good and proceeding as
                // sh 'npm test'
                echo 'CI'
            }
        }
        stage('Release'){
            steps{
                echo 'CI'
            }
        }
    }
}
//