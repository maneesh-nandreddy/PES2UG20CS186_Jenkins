pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o PES2UG20CS186-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './PES2UG20CS186-1'
        }
     stage('Deploy') {
        steps {
            // deployment code
            sh 'mvn deploy'
            echo 'deployment successful'
        }    
    }
}

post {
    always {
        echo 'Pipeline completed'
    }
    failure {
        echo 'Pipeline failed'
    }
}
}
