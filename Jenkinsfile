pipeline {
    agent any

    tools {
        maven 'maven-3.9.0'
        jdk 'jdk-17'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ShalabhRanjan19/MymavenApp01.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy WAR') {
            steps {
                // Replace with your actual remote details
                sh '/home/shalabh/MymavenWebApp01/target/'
            }
        }
    }
}
