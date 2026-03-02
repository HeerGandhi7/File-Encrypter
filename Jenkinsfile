node('agent1') {
    stage('Build') {
        echo "Building Java project..."
        sh '''
            cd "Password Protection"
            mkdir -p build
            javac -d build src/*.java
            echo "Build successful"
        '''
    }

    stage('Test') {
        echo "Running dummy test..."
        sh 'echo "Test successful"'
    }

    stage('Deploy') {
        echo "Packaging application..."
        sh '''
            cd "Password Protection"
            jar cf FileEncrypter.jar -C build .
            echo "Deployment successful"
        '''
    }
}
