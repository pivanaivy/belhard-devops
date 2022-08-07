pipeline { agent {label 'docker'} stages { stage("Initial config") 
        {
            steps { script { 
                    properties([pipelineTriggers([pollSCM('* * * * 
                    *')])])
                }
           }
        }
                stage('Checkout') { steps{ git branch: 'Test', url: 
                    'https://github.com/pivanaivy/Project.git'
                }
        }
        stage("start docker-compose") { steps { sh ''' echo $USER 
                pwd ls -la cd classsed-docker-tutorial 
                docker-compose up --build -d '''
                }
            }
        }
    }
