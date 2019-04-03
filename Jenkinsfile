pipeline {
    agent none
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            
           steps {
                echo 'Deploying the built lah'
               withSonarQubeEnv('SonarQube') {
                    // some block
                }
            }
        }
    }
}


