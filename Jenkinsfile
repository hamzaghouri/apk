pipeline {
    agent any
        parameters {
        choice(choices:'alpha\nbeta\nproduction',description: 'Select Release Track If you are not sure choose alpha', name: 'RELEASE_TRACK')
        string(defaultValue: '', description: 'Latest Release Name is required e.g (2.28.0)',  name: 'RELEASE_NAME')
        string(defaultValue: '10', description: 'Delivery name',  name: 'ROLLOUT_PERCENT')
    }
    stages {
        stage('Test') {
            steps {
              echo "Rollout Percentage :${ROLLOUT_PERCENT}"
              echo "RELEASE_NAME : ${ROLLOUT_PERCENT}"
              echo 'Testing application..'
              echo 'Step skipped for now'
        
          stage('Build APK & AAB') {
              steps {
                echo 'Copying settings scripts'
         
              }
            
          }

       /stage('Pushing AAB to S3') {
         steps {
           echo 'Pushing APK to s3'
         // sh 'cp android/app/build/outputs/bundle/release/app-release.aab hisaab-prod.aab'
            //sh 'aws s3 cp hisaab-prod.aab s3://cb-jenkins-bucket/apk_builds/prod/hisaab-prod$(date -d "today" +"%H-%M-%m-%d-%Y").aab'
       }
         
      }



        // stage('Upload APK') {
          // steps {
            // Upload the APK to Google Play
           // androidApkUpload filesPattern: 'hisaab-prod.aab', googleCredentialsId: 'CreditBook', releaseName: "${RELEASE_NAME}", rolloutPercentage: "${ROLLOUT_PERCENT}", trackName: "${RELEASE_TRACK}"
          // }
           
    //}
}
