pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm start"
            }
        }
        stage("Deploy") {
            steps {
                sh "rm -rf /var/www/jenkins-react-app"
                sh "cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
