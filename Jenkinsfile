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
            }
        }
        
        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
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
            echo 'allways post message'
        }
        
        success {
            echo 'post success message'   
        }
        
        unstable {
            echo 'post unstable message'   
        }
        
        failure {
            echo 'post fail message'   
        }
        
        changed {
            echo 'post -things were changed message'   
        }
        
    }
    
    
}

