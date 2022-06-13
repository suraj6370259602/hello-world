# hello-world
pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo "Hello world"
                    }
            }
        }
    post{
        always{
            mail to: "surajnayak301301@gmail.com",
            subject: "Test Email",
            body: "Test"
        }
    }
}
