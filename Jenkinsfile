pipeline {
    environment {
        FOO = "BAR"
    }

    agent { label "master" }

    stages {
        stage("test01") {
            steps {
                sh 'echo "01.FOO is ${FOO}"'
            }
        }
        stage("test02") {
            steps {
                sh 'echo "02.FOO is ${FOO}"'
            }
        }
    }
}
