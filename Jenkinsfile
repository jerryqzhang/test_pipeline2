pipeline {
    environment {
        FOO2 = "BAR2"
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    agent { label "master" }

    stages {
        stage("test01") {
            steps {
                echo "01.FOO is ${FOO2}"
            }
        }
        stage("test02") {
            environment {
                FOO3 = "BAR3"
            }      
            steps {
                echo "02.FOO is ${FOO2}"
                echo "02.FOO is ${FOO2}"
                echo "02.FOO is ${FOO2}"
                echo "02-1.FOO is ${FOO3}"
            }
        }
        stage("test03") {
            steps {
                echo "02.FOO is ${FOO2}"
                echo "Hello ${params.PERSON}"
                script {
                    def browsers = "test_browsers"
                }
            }
        }
    }
}
