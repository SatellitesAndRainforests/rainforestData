pipeline {
    
    agent any
    

    
    stages {
        
        stage('build') {
            steps {
                sh 'echo "hello from jenkinsfile"'
                sh '''
                    echo "mutliline shelll steps work too"
                    ls -lah
                '''
            }
        }
        
        stage('nextstate') {
            steps {
                sh 'echo "hello from next state"'
            }
        }
            
        stage('one') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './gradlew check'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        
    }
    
    
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
    
    
}
