pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                echo 'hello from master-2 branch.'
                bat 'git rev-parse --abbrev-ref HEAD'

                script {
                    echo 'testing.  ..'

                    

                    try {
                        echo scm.branches[0].name
                    } catch(Exception e) {
                        echo 'Fail 1'
                    }

                    try {
                        echo scm.branches.first().getExpandedName(env.getEnvironment())
                    } catch(Exception e) {
                        echo 'Fail 2'
                    }
                }
            }
        }
    }
}