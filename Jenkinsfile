pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                echo 'Starting pipeline from main Jenkinsfile'
            }
        }
        stage('Run Shared Pipeline') {
            steps {
                script {
                    if (fileExists('ci/pipeline.groovy')) {
                        load 'ci/pipeline.groovy'
                    } else {
                        echo 'No shared pipeline script found; running default step.'
                    }
                }
            }
        }
    }
}
