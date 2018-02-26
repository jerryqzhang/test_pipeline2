pipeline {
    environment {
        FOO2 = "BAR2"
    }

    agent { label "master" }

    stages {
        stage("test01") {
            steps {
                echo "01.FOO is ${FOO2}"
            }
        }
        stage("test02") {
            steps {
                FOO2 = "BAR3"
                echo "02.FOO is ${FOO2}"
            }
        }
        stage("test03") {
            steps {
                echo "02.FOO is ${FOO2}"
            }
        }
    }
}
