pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Build') {           
                steps {
                // Get some code from a GitHub repository
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }    
        
        }
        stage('Build') {           
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/belagrun/jenkins.git'
                sh 'mvn clean package -DskipTests=true'
            }


        }

        stage('Unit Test')
        {
            steps {
                sh  mvn test'
            }
            
        }
    }
}
