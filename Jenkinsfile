pipeline {
    agent any
    stages {
        stage ('Lint HTML') {
            steps {
                withAWS(region:'us-west-2',credentials:'aws-static') {
                    sh '''
                        tidy -q -e *.html
                    '''
                }
            }
        }
        stage ('Upload to AWS') {
            steps {
                withAWS(region:'us-west-2',credentials:'aws-static') {
                    sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                    '''
                    sh 'ls -ld'
                    s3Upload(file:'index.html', bucket:'jenkins-build-devops', path:'index.html')
                }
            }

        }
    }
}
