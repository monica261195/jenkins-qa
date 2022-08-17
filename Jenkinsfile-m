pipeline {
    agent any
    parameters {
        string(name: 'BRANCH', description: 'Enter the branch to build', defaultValue: '')
                }
    environment {
                GIT_REPO = "https://github.com/monica261195/jenkins-qa"
                }
    
     stages {
        stage ("Test1") {
            when {
                expression {
                    params.BRANCH == 'main' || params.BRANCH == 'branch1'
            steps {
                echo "HI"
            }
                }
            }
        }

        stage ("Test2") {
            steps {
                script {
                    if(params.BRANCH == 'main')
                    {
                        git branch: params.BRANCH, url: env.GIT_REPO
                        sh 'echo "This is a test2 stage"'   
                        
                    } else { 
                        sh 'exit1'    
                    }  
                    
                }
            }
        }


     }  
}
