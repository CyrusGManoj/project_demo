pipeline {
    agent any 
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/CyrusGManoj/project_demo.git', branch: 'main' 
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    def app = docker.build("demo-run") 
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    app.run()
                }
            }
        }
    }
}