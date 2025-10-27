pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                echo 'Checking out the code from anne-marie branch...'
                checkout scm
            }
        }
        stage('Hello'){
            steps{
                echo 'Hello, World! from anne-marie branch.'
            }       
        }
        stage('User Input'){
            steps{
                script {
                    input message: 'This is anne-marie branch. Do you want to continue?', 
                    ok: 'Yes'
                }
            }
        }
        stage('Goodbye'){
            steps{
                echo 'Goodbye from anne-marie branch.'
            }       
        }
    }

    post{
        always {
            echo 'This will always run after the pipeline completes.'
        }
    }
}





