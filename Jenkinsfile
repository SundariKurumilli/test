pipeline {
    agent any
    environment {
        buildDir = "/var/lib/jenkins/workspace/Package_Deploy_Pipeline/"
    }
    stages {
        stage('Upload') {
            steps {
                sh 'curl -v --user user:password --data-binary ${buildDir}package${env.BUILD_NUMBER}.tar -X PUT "http://artifactory.mydomain.com/artifactory/release-packages/package${env.BUILD_NUMBER}.tar"'
            }
        }
    }
}
