pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             withAWS(region:'us-west-2',credentials:'aws-static') {
                 steps {
                    sh 'echo "Hello World"'
                    sh '''
                         echo "Multiline shell steps works too"
                         ls -lah
                    '''
                 }
              }
         }
     }
}
