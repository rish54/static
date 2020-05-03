pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
              steps {
                  withAWS(region:'eu-west-1',credentials:'AWSJenkins') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacitystaticwebsitebucket')
                  }
         }
    }
    }
}   
