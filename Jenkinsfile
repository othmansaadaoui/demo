pipeline{
    agent any

environment {
    DEM0= '1.3'
}
    stages{
        stage('stage1') {
            steps{
                echo "THIS iS BUILD N  $BUILD_NUMBER of demo "
                sh '''
                    echo "Using a mltiline shell step"
                    chmod +x test.sh 
                    
                '''

            }
            
        }
    }
    
}


