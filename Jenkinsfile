pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             steps {
                 withAWS(region:'us-west-2',credentials:'aws-static') {
                     sh 'echo "added s3Upload()"'
                     sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                     '''
                     s3Upload(file:'index.html', bucket:'jenkins-build-devops', path:'./index.html')
                }
            }
        }
    }
}
