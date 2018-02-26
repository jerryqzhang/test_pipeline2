pipeline {
    environment {
        FOO2 = "BAR2"
    }

    agent { label "master" }

    stages {
        stage("test01") {
            steps {
                def FOO1 = "BAR1"
                echo "00.FOO is ${FOO1}"
                echo "01.FOO is ${FOO2}"
            }
        }
        stage("test02") {
            steps {
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
