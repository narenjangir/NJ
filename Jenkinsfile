pipeline 
{
    agent any
    stages{    
    
stage('SonarQube') {
    steps{
        withSonarQubeEnv('SonarQube') {
            sh "/var/jenkins_home/sonar-scanner/sonar-scanner-3.3.0.1492-linux/bin/sonar-scanner -Dsonar.projectKey=sonar_project"
        }
        timeout(time: 10, unit: 'MINUTES') {
            waitForQualityGate abortPipeline: true
        }
    }
}
    }}
