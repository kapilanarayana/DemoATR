pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
                git 'https://github.com/kapilanarayana/DemoATR.git'
            }
        }
         stage('continuous build') {
            steps {
                sh 'mvn install'
            }
        }
         stage('continuous deploy') {
            steps {
                sh 'cp target/DemoATR.war /opt/apache-tomcat-9.0.62/webapps'
            }
        }
    }
}
