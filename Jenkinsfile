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
        
        success {
            echo 'post success message'   
        }
        
        unstable {
            echo 'post unstable message'   
        }
        
        failure {
            echo 'post fail message'   
            mail    to: 'mark@rakocontrols.com',
                    subject: "from jenkins pipleline post 'fail': ${currentBuild.fullDisplayName}",
                    body: "from jenkins ${env.BUILD_URL}"
        }
        
        changed {
            echo 'post -things were changed message'   
        }
        
    }
    
    
}
