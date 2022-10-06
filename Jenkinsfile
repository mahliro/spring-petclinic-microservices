pipeline
{
    agent {
     // node { label 'EC2' }
            docker {
                 image 'maven:3-alpine'
                 args '-v /root/.m2:/root/.m2'
            }
           }
    stages {
        stage('Unit Test') {
            steps {
                sh 'mvn clean package -Dmaven.test.skip=true'
                archiveArtifacts(artifacts: '**/*.jar', onlyIfSuccessful: true, fingerprint: true)
                  }
                        }
    }
}


