pipeline {
    agent any
    stages {
        stage('Cloning Git') {
            steps {
                git branch: 'master', url: 'http://github.com/martin-scantist/intentionally-vulnerable-golang-project/'
                echo "Git cloned!"
                }
        }
        stage ('Scantist') {
            steps {
                sh '''
                    ls
                    pwd
                    curl -s https://download.scantist.io/scantist-bom-detect.jar --output scantist-bom-detect.jar
                    java -jar scantist-bom-detect.jar
                '''
            }
        }
    }
}
