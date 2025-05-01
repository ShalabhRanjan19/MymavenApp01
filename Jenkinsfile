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
                // Copy WAR to Tomcat's webapps folder using sudo
                sh 'sudo cp target/MymavenWebApp01.war /opt/tomcat/webapps/'
            }
        }
    }
}
