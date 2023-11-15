pipeline {
    
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    echo 'Hello World'
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
