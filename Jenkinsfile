pipeline {
    environment {
        FOO = "BAR"
    }

    agent { label "master" }

    stages {
        stage("foo") {
            steps {
                sh 'echo "FOO is $FOO"'
            }
        }
    }
}
