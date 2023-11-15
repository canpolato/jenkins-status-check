pipeline {
    
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    echo 'Hello World'
                    if (env.CHANGE_ID) { // otherwise the object is not defined
                        echo pullRequest.title
                    }
                }
            }
        }
    }
}
