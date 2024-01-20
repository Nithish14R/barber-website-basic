pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your Git repository
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Deploy') {
            steps {
                // This assumes you have a web server configured on your Jenkins machine
                // Copy the HTML/CSS files to the web server directory
                sh 'cp -r * /path/to/your/webserver/directory'
            }
        }
    }

    post {
        success {
            // Actions to be taken when the build is successful
            echo 'Deployment successful! You can add notifications or additional steps here.'
        }
        failure {
            // Actions to be taken when the build fails
            echo 'Deployment failed! You can add notifications or additional steps here.'
        }
    }
}
