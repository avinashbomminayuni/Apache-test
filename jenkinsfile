pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your GitHub repository
                git 'https://github.com/avinashbomminayuni/Apache-test.git'
            }
        }
        
        stage('Build and Deploy') {
            steps {
                // Add your build steps here if needed
                
                // Copy your web files to Apache's document root
                sh 'cp -r * /var/www/html/'
                
                // Restart Apache to apply changes
                sh 'sudo systemctl restart apache2'  // Adjust the command based on your server setup
            }
        }
    }
    
    post {
        success {
            echo 'Deployment successful!'
        }
    }
}

