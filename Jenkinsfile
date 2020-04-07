pipeline {
    agent any
    stages {
        stage('Lint HTML') {
            steps {
                sh 'tidy -q -e *.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'aws-static') {

                s3Upload(file:'index.html', bucket:'project4jenkins', path:'C:/Users/Usuario/Desktop/EmailUp/Proyecto #4/index.html');
                }
            }
        }
    }
}