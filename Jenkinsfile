pipeline {
    agent {
        docker {
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') { 
            steps {
                 sh 'mvn test' 
            }
        }
    }
}
