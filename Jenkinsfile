pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2',credentials:'aws-static') {
                    s3Upload(bucket:"tmk-udc-proj4", path:'/', includePathPattern:'**/*', workingDir:'.', excludePathPattern:'**/*Jenkinsfile')
                }
            }
        }
    }
}
