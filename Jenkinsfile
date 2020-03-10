pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             withAWS(region:'us-west-2',credentials:'aws-static') {
                 steps {
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
