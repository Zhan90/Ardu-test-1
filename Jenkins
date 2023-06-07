pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/Zhan90/Ardu-test-1.git'
                sh '''
                    ls -la
                    cat read_test.txt
                    cat readme.txt
                    arduino-cli core list
                    arduino-cli core install arduino:samd
                    arduino-cli compile --fqbn arduino:samd:mkr1000 Blink
                    arduino-cli board list
                '''
            }
        }
    }
}
