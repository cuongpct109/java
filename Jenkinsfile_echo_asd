pipeline{
    agent any
    parameters {
        booleanParam(name: "Build", defaultValue: true)
        booleanParam(name: "Restart", defaultValue: false)
        booleanParam(name: "Shutdown", defaultValue: false)
        booleanParam(name: "Scan", defaultValue: false)
    }
    stages{
        stage("Shutdown"){
            when { expression {return "$params.Build" == 'false' && "$params.Restart" == 'false' && "$params.Shutdown" == 'true' && "$params.Scan" == 'false' }}
            steps{
                script{
                    sh "echo Shutdown something"
                }
            }
            post {
                success {
                    script{
                        sh "echo Shutdown success"
                    }
                }
                failure {
                    script{
                        sh "exit 1"
                        //or
                        error "Failed, exiting now..."
                    }
                }
            }
        }


    }
}
