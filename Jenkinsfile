pipeline
{
    agent {
      node { label 'EC2' }
           }
    stages {
        stage('Unit Test') {
            steps {
                sh 'mvn clean package -Dmaven.test.skip=true'
                  }
                        }
    }
}


