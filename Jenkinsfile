stage ('Scantist') {
            steps {
                sh '''
                    curl -s https://download.scantist.io/scantist-bom-detect.jar --output scantist-bom-detect.jar
                    java -jar scantist-bom-detect.jar
                '''
            }
        }
