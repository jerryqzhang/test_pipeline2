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
                echo "03.FOO is ${FOO2}"
                echo "Hello ${params.PERSON}"
                script {
                    FOO2 = "be_changed"
                    def browsers = "test_browsers"
                    echo "04.FOO is ${browsers}"
                    echo "05.changed_FOO2 is ${FOO2}"
                }
                input message: 'Finished output after statements? (Click "Proceed" to continue)'
                echo "06.changed_FOO2 is ${FOO2}"
            }
        }
        stage("test04") {
            parallel{
                stage("branch_01"){
                    steps {
                        echo "07.changed_FOO2 is ${FOO2}"
                    }
                }
                stage("branch_02"){
                    steps {
                        echo "08.changed_FOO2 is ${FOO2}"
                    }
                }
            }
            stage("branch_03"){
                    steps {
                        echo "09.changed_FOO2 is ${FOO2}"
                    }
            }

        }
    }
}
