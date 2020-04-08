pipeline {
    agents any
    stages {
        stage("Creating useless files") {
            steps {
                sh """
                    touch file{1..10}
                """
            } //step
        } //stage
        stage("Run helloworld.py") {
            steps {
                sh """
                    python3 helloworld.py
                """
            } //step
        } //stage
    } //stages
    post {
        always {
            sh """
                rm -rf file{1..10}
            """
        }
    }
} //pipeline