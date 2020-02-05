pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') {
            environment {
                SERVICE_CREDS = credentials('install:Lvon!476')
            }
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
