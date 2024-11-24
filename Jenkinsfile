pipeline {
    agent any

    parameters {
        string(name: 'FILE_CONTENT', defaultValue: 'Hello, Jenkins!', description: 'Enter the content for the file')
        choice(name: 'DEPLOY_ENV', choices: ['Development', 'Staging', 'Production'], description: 'Select the deployment environment')
        string(name: 'NAME', defaultValue: '', description: 'Enter your name')
        choice(name: 'EXPERIENCE', choices: ['less than 1', '+1', '+2', '+3', '+4'], description: 'Select your experience')
    }

    stages {
        stage('Print Output') {
            steps {
                script {
                    def name = params.NAME
                    def experience = params.EXPERIENCE
                    echo "Your name is ${name} and you have ${experience} years of experience"
                }
            }
        }

        stage('Setup File') {
            steps {
                script {
                    def fileContent = params.FILE_CONTENT
                    writeFile file: 'myfile.txt', text: fileContent
                    echo "File 'myfile.txt' created with content: ${fileContent}"
                }
            }
        }

        stage('Test File Content') {
            steps {
                script {
                    def fileContent = readFile('myfile.txt').trim()
                    if (fileContent == params.FILE_CONTENT) {
                        echo "Test passed: Content '${fileContent}' matches the parameter."
                    } else {
                        error "Test failed: Content in file does not match parameter!"
                    }
                }
            }
        }

        stage('For Loop Example') {
            steps {
                script {
                    for (int i = 1; i <= 5; i++) {
                        echo "Iteration ${i}"
                    }
                }
            }
        }

        stage('For Loop List') {
            steps {
                script {
                    def mylist = ["apple", "orange", "blueberry", "banana", "watermelon"]
                    for (String fruit : mylist) {
                        echo "Fruit ==> ${fruit}"
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    def environment = params.DEPLOY_ENV
                    echo "Starting deployment to ${environment} environment..."
                    sleep(time: 2, unit: 'SECONDS')
                    echo "Deployment to ${environment} completed successfully!"
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed!'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
