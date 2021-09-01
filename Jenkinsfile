pipeline {
    
    agent { none  }
    
    enviroment {
        DISABLE_AUTH = 'true'
        DB_ENGINE = 'postgresql'
    }
    
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
                echo "database engine is $DB_ENGINE}"
                echo "DISABLE_AUTH os ${DISABLE_AUTH}"
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
    
    
    
}
