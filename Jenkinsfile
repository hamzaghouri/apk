pipeline {
    agent any
    stages {
        stage('Test') {
            steps {

              echo 'Testing application..'
              echo 'Step skipped for now'
            }
            }
          stage('Build APK & AAB') {
              steps {
                echo 'Copying settings scripts'
         
              }
          }

       stage('Pushing AAB to S3') {
         steps {
           echo 'Pushing APK to s3'
         // sh 'cp android/app/build/outputs/bundle/release/app-release.aab hisaab-prod.aab'
            //sh 'aws s3 cp hisaab-prod.aab s3://cb-jenkins-bucket/apk_builds/prod/hisaab-prod$(date -d "today" +"%H-%M-%m-%d-%Y").aab'
       }
         
      }



         stage('Upload APK playstore') {
           steps {
               echo 'Uploading to Playstore'
            // Upload the APK to Google Play
           // androidApkUpload filesPattern: 'hisaab-prod.aab', googleCredentialsId: 'CreditBook', releaseName: "${RELEASE_NAME}", rolloutPercentage: "${ROLLOUT_PERCENT}", trackName: "${RELEASE_TRACK}"
           }
           
    }
}
}
