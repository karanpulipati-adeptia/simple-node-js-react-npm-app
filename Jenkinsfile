pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from your Git repository
                git 'https://github.com/yourusername/your-react-project.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Use Node.js installation defined in Jenkins NodeJS plugin
                // Make sure to configure the NodeJS installation in Jenkins global tool configuration
                // This assumes 'node' and 'npm' commands are available in the PATH
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                // Build your React.js project
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests if you have any
                // Example using Jest:
                // sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deployment steps
                // Example: Copy files to a server, deploy to a cloud platform, etc.
            }
        }
    }
    
    post {
        always {
            // Clean up or any other post-processing tasks
        }
    }
}
