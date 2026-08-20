pipeline {
    agent {
        docker {
            image 'postman/newman:latest' 
            args '--entrypoint='
        }
    }

    stages {
        stage('lancement de la collection') {
            steps {
                script {
                        sh "newman run postman_cicd_collection.json -e preprod_environment.json"
                }
            }
        }
    }
}
