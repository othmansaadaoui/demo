pipeline {
    agent any
    environment {
        DEMO='1.6'
}


    stages {
        stage('Hello') {
            steps {
                echo "This is build number $BUILD_NUMBER of demo $BUILD"
                sh '''
                    echo "USING a multi-line shell "
                    chmod +x test.sh
                    ./test.sh
            }
        }
    }
}
