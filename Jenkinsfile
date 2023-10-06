pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}


pipeline{
    agent any
       tools{
        nodejs "Node12"
       }
    stages{
        stage("Build"){
            steps{
                echo "========executing Build========"
                sh "npm install"
            }
        }
         stage("Test"){
            steps{
                echo "========executing Test========"
                sh "npm test"
                sh "pwd"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
