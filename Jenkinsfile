pipeline {
    agent any

    stages {
        stage('test') {
            steps {
                script {
                    echo 'testing.  ..'

                    git branch

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