pipeline {
    
    agent any

    stages {
        stage('CR Validation Check') {
            steps {
                script {
                    echo 'CR Validation Check'
                    if (env.CHANGE_ID) { // otherwise the object is not defined
                        if (pullRequest.title = 'ValidCR') {
                            echo 'CR id valid'
                        } else {
                            echo 'CR is invalid'
                            error('Aborting....')
                        }
                    }
                }
            }
        }
    }
}
