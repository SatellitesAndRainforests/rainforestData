pipeline {
    
    agent { docker { image 'maven:3.3.3' } }
    
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
        
    }
    
    
    
}
