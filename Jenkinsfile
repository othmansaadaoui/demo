pipeline {
    agent any
    environment {
        RELEASE='20.04'
    }
    stages {
        stage('Build') {
            agent any
            environment {
                LOG_LEVEL='INFO'
            }
            steps {
                echo "Building release ${RELEASE} with log level ${LOG_LEVEL}..."
            }
        }
        stage('Test') {
            steps {
                echo "Testing release ${RELEASE}..."
            }
        }
        

        stage('Deploy'){

            input{
                
                message 'Deploy?'
                ok 'do it!'
                parameters{

                    string(name: 'TARGET_ENVIRONMENT', defaultValue:'PROD', description: 'TARGET deployement environemnt')

                }
                
            }
            steps{
                echo "Deploying release ${release} to environment ${TARGET_ENVIRONMENT}"
            }
        }

    }
    post{
        always{
            echo 'PRINT whether deploy happend or not , succes or failure '
        }
    }
}