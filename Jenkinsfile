pipeline {
    agent any
    environment {
                GIT_REPO = "https://github.com/monica261195/jenkins-qa"
                }
    parameters {
        string(name: 'BRANCH', description: 'Enter the branch to build', defaultValue: 'null')
                }
     stages {
        stage ("Test1") {
            steps {
                script {
                    if(params.BRANCH == 'main')
                    {
                        git branch: params.BRANCH, url: env.GIT_REPO
                        sh '''
                            #!/bin/bash 
                            pwd 
                            ls
                            echo "This is a test1 stage"
                            
                        '''
                    } else { 
                        echo "Skipping test1 stage ....."    
                    }  
                }
            }
        }
     }  
}
