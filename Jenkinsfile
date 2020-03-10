pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             steps {
                 withAWS(region:'us-west-2',credentials:'aws-static') {
                     sh 'echo "added withAWS()"'
                     sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                     '''
                }
            }
        }
    }
}
