pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/aespinosa221120/simple-maven-project-with-tests.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Long Running Work') {
            steps {
                echo 'Sleeping for 1000 seconds...'
                sleep 1000
            }
        }

        stage('Post Build') {
            steps {
                echo 'Build Finished!'
            }
        }
    }
}
