pipeline {
    agent any
    parameters {
        string(name: 'BRANCH', description: 'Enter the branch to build', defaultValue: 'null')
                }
    environment {
                GIT_REPO = "https://github.com/monica261195/jenkins-qa"
                }
    
     stages {
        stage ("Test1") {
            steps {
                script {
                    if(params.BRANCH == 'master')
                    {
                        git branch: params.BRANCH, url: env.GIT_REPO
                        sh 'echo "This is a test1 stage in master branch"'     
                    } 
                    else { 
                        echo "Skipping test1 stage ....."    
                    }  

                }
            }
        }

        stage ("Test2") {
            steps {
                script {
                    if(params.BRANCH == 'master')
                    {
                        git branch: params.BRANCH, url: env.GIT_REPO
                        sh 'echo "This is a test2 stage in master branch"'     
                    }
                    else { 
                        echo "This is not master branch "    
                    }  
                    
                }
            }
        }
     }  
}
